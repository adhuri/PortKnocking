default: executable

executable:
	@echo "		Setting chmod permission to executable for backdoor knocker and read permission for configuration"
	chmod +x backdoor
	chmod +x knocker
	chmod +r configuration-file
	@echo "		Done"

help:
	@echo "    executable"
	@echo "        Gives chmod +x permission on the current host to all required files"
	@echo "    readonly"
	@echo "        Gives chmod 444 permission on the current host to all required files "

clean: readonly remove-pyc

readonly:
	@echo "		Setting chmod permission to read only "
	chmod 444 backdoor
	chmod 444 knocker
	chmod 444 configuration-file
	@echo "		Done"

remove-pyc:
	@echo "		Removing .pyc files "
	find . -name '*.pyc' -exec rm --force {} +
	find . -name '*.pyo' -exec rm --force {} +
	@echo "		Done "
