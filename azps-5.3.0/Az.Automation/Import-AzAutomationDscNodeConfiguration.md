---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: CC9D74BB-DFB2-41F3-B5CF-B265C549EC33
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/import-azautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Import-AzAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Import-AzAutomationDscNodeConfiguration.md
ms.openlocfilehash: 3036b02d280542ffa4c8eea85dafed2da8eb5e28
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502332"
---
# <span data-ttu-id="37e20-101">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="37e20-101">Import-AzAutomationDscNodeConfiguration</span></span>

## <span data-ttu-id="37e20-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="37e20-102">SYNOPSIS</span></span>
<span data-ttu-id="37e20-103">Importuje dokument MOF jako konfigurację węzła DSC w automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="37e20-103">Imports a MOF document as a DSC node configuration in Automation.</span></span>

## <span data-ttu-id="37e20-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="37e20-104">SYNTAX</span></span>

```
Import-AzAutomationDscNodeConfiguration -Path <String> -ConfigurationName <String> [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncrementNodeConfigurationBuild] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37e20-105">Opis</span><span class="sxs-lookup"><span data-stu-id="37e20-105">DESCRIPTION</span></span>
<span data-ttu-id="37e20-106">Polecenie cmdlet **Import-AzAutomationDscConfiguration** importuje dokument konfiguracji Managed Object Format (MOF) do usługi Azure Automation jako konfigurację wybranego węzła konfiguracji stanu (DSC).</span><span class="sxs-lookup"><span data-stu-id="37e20-106">The **Import-AzAutomationDscConfiguration** cmdlet imports a Managed Object Format (MOF) configuration document into Azure Automation as a Desired State Configuration (DSC) node configuration.</span></span>
<span data-ttu-id="37e20-107">Określ ścieżkę pliku MOF.</span><span class="sxs-lookup"><span data-stu-id="37e20-107">Specify the path of a .mof file.</span></span>

## <span data-ttu-id="37e20-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="37e20-108">EXAMPLES</span></span>

### <span data-ttu-id="37e20-109">Przykład 1: Importowanie konfiguracji węzła DSC do automatyzacji</span><span class="sxs-lookup"><span data-stu-id="37e20-109">Example 1: Import a DSC node configuration into Automation</span></span>
```
PS C:\>Import-AzAutomationDscNodeConfiguration -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ConfigurationName "ContosoConfiguration" -Path "C:\DSC\webserver.mof" -Force
```

<span data-ttu-id="37e20-110">To polecenie importuje konfigurację węzła DSC z pliku WebServer. MOF do konta usługi Automation o nazwie Contoso17 pod nazwą konfiguracji DSC ContosoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="37e20-110">This command imports a DSC node configuration from the file named webserver.mof into the Automation account named Contoso17, under the DSC configuration ContosoConfiguration.</span></span>
<span data-ttu-id="37e20-111">Polecenie określa parametr *Force* .</span><span class="sxs-lookup"><span data-stu-id="37e20-111">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="37e20-112">Jeśli istnieje konfiguracja węzła DSC o nazwie ContosoConfiguration. WebServer, to polecenie zamieni je.</span><span class="sxs-lookup"><span data-stu-id="37e20-112">If there is an existing DSC node configuration named ContosoConfiguration.webserver, this command replaces it.</span></span>

### <span data-ttu-id="37e20-113">Przykład 2: Importowanie konfiguracji węzłów DSC do automatyzacji i tworzenie nowej wersji kompilacji bez zastępowania istniejących NodeConfiguration.</span><span class="sxs-lookup"><span data-stu-id="37e20-113">Example 2: Import a DSC node configuration into Automation and create a new build version and not overwrite existing NodeConfiguration.</span></span>
```
PS C:\>Import-AzAutomationDscNodeConfiguration -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ConfigurationName "ContosoConfiguration" -Path "C:\DSC\webserver.mof" -IncrementNodeConfigurationBuild
```

<span data-ttu-id="37e20-114">To polecenie importuje konfigurację węzła DSC z pliku WebServer. MOF do konta usługi Automation o nazwie Contoso17 pod nazwą konfiguracji DSC ContosoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="37e20-114">This command imports a DSC node configuration from the file named webserver.mof into the Automation account named Contoso17, under the DSC configuration ContosoConfiguration.</span></span>
<span data-ttu-id="37e20-115">Polecenie określa parametr *Force* .</span><span class="sxs-lookup"><span data-stu-id="37e20-115">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="37e20-116">Jeśli istnieje konfiguracja węzła DSC o nazwie ContosoConfiguration. WebServer, to polecenie doda nową wersję kompilacji o nazwie ContosoConfiguration [2]. WebServer.</span><span class="sxs-lookup"><span data-stu-id="37e20-116">If there is an existing DSC node configuration named ContosoConfiguration.webserver, this command adds a new build version with the name ContosoConfiguration[2].webserver.</span></span>

## <span data-ttu-id="37e20-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="37e20-117">PARAMETERS</span></span>

### <span data-ttu-id="37e20-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="37e20-118">-AutomationAccountName</span></span>
<span data-ttu-id="37e20-119">Określa nazwę konta automatyzacji, do którego jest zaimportowana konfiguracja węzła DSC przy użyciu tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37e20-119">Specifies the name of the Automation account into which this cmdlet imports a DSC node configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37e20-120">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="37e20-120">-ConfigurationName</span></span>
<span data-ttu-id="37e20-121">Określa nazwę konfiguracji DSC w automatyzacji, która ma być używana jako obszar nazw i kontener konfiguracji węzła do zaimportowania.</span><span class="sxs-lookup"><span data-stu-id="37e20-121">Specifies the name of a DSC configuration in Automation to use as the namespace and container for the node configuration to import.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37e20-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37e20-122">-DefaultProfile</span></span>
<span data-ttu-id="37e20-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="37e20-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37e20-124">-Force</span><span class="sxs-lookup"><span data-stu-id="37e20-124">-Force</span></span>
<span data-ttu-id="37e20-125">Wskazuje, że to polecenie cmdlet zastępuje istniejącą konfigurację węzła DSC w automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="37e20-125">Indicates that this cmdlet replaces an existing DSC node configuration in Automation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37e20-126">-IncrementNodeConfigurationBuild</span><span class="sxs-lookup"><span data-stu-id="37e20-126">-IncrementNodeConfigurationBuild</span></span>
<span data-ttu-id="37e20-127">Tworzy nową wersję kompilacji konfiguracji węzła.</span><span class="sxs-lookup"><span data-stu-id="37e20-127">Creates a new Node Configuration build version.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37e20-128">-Path</span><span class="sxs-lookup"><span data-stu-id="37e20-128">-Path</span></span>
<span data-ttu-id="37e20-129">Określa ścieżkę dokumentu konfiguracji MOF, który został zaimportowany za pomocą tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37e20-129">Specifies the path of the MOF configuration document that this cmdlet imports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37e20-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37e20-130">-ResourceGroupName</span></span>
<span data-ttu-id="37e20-131">Określa nazwę grupy zasobów, dla której to polecenie cmdlet importuje konfigurację węzła DSC.</span><span class="sxs-lookup"><span data-stu-id="37e20-131">Specifies the name of a resource group for which this cmdlet imports a DSC node configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37e20-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="37e20-132">-Confirm</span></span>
<span data-ttu-id="37e20-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37e20-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37e20-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37e20-134">-WhatIf</span></span>
<span data-ttu-id="37e20-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37e20-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37e20-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="37e20-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37e20-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37e20-137">CommonParameters</span></span>
<span data-ttu-id="37e20-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37e20-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37e20-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37e20-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37e20-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="37e20-140">INPUTS</span></span>

### <span data-ttu-id="37e20-141">System. String</span><span class="sxs-lookup"><span data-stu-id="37e20-141">System.String</span></span>

## <span data-ttu-id="37e20-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="37e20-142">OUTPUTS</span></span>

### <span data-ttu-id="37e20-143">Microsoft. Azure. Commands. Automation. model. NodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="37e20-143">Microsoft.Azure.Commands.Automation.Model.NodeConfiguration</span></span>

## <span data-ttu-id="37e20-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="37e20-144">NOTES</span></span>

## <span data-ttu-id="37e20-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="37e20-145">RELATED LINKS</span></span>

[<span data-ttu-id="37e20-146">Eksportowanie — AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="37e20-146">Export-AzAutomationDscConfiguration</span></span>](./Export-AzAutomationDscConfiguration.md)

[<span data-ttu-id="37e20-147">Get-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="37e20-147">Get-AzAutomationDscConfiguration</span></span>](./Get-AzAutomationDscConfiguration.md)


