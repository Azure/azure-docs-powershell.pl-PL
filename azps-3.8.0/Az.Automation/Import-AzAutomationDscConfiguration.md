---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: BA508F0B-847F-4531-9D5D-A5A044A2D207
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/import-azautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Import-AzAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Import-AzAutomationDscConfiguration.md
ms.openlocfilehash: 21b3e8c29d9d74f548ca9d212a72d4b70520aa82
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053949"
---
# <span data-ttu-id="ebd87-101">Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="ebd87-101">Import-AzAutomationDscConfiguration</span></span>

## <span data-ttu-id="ebd87-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ebd87-102">SYNOPSIS</span></span>
<span data-ttu-id="ebd87-103">Importuje konfigurację DSC do automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="ebd87-103">Imports a DSC configuration into Automation.</span></span>

## <span data-ttu-id="ebd87-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ebd87-104">SYNTAX</span></span>

```
Import-AzAutomationDscConfiguration -SourcePath <String> [-Tags <IDictionary>] [-Description <String>]
 [-Published] [-Force] [-LogVerbose <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ebd87-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ebd87-105">DESCRIPTION</span></span>
<span data-ttu-id="ebd87-106">Polecenie cmdlet **Import-AzAutomationDscConfiguration** importuje konfigurację konfiguracji pożądanego stanu (DSC) do usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="ebd87-106">The **Import-AzAutomationDscConfiguration** cmdlet imports an APS Desired State Configuration (DSC) configuration into Azure Automation.</span></span>
<span data-ttu-id="ebd87-107">Określ ścieżkę do skryptu APS, który zawiera jedną konfigurację DSC.</span><span class="sxs-lookup"><span data-stu-id="ebd87-107">Specify the path of an APS script that contains a single DSC configuration.</span></span>

## <span data-ttu-id="ebd87-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ebd87-108">EXAMPLES</span></span>

### <span data-ttu-id="ebd87-109">Przykład 1: Importowanie konfiguracji DSC do automatyzacji</span><span class="sxs-lookup"><span data-stu-id="ebd87-109">Example 1: Import a DSC configuration into Automation</span></span>
```
PS C:\>Import-AzAutomationDscConfiguration -AutomationAccountName "Contoso17"-ResourceGroupName "ResourceGroup01" -SourcePath "C:\DSC\client.ps1" -Force
```

<span data-ttu-id="ebd87-110">To polecenie powoduje zaimportowanie konfiguracji DSC z pliku o nazwie client.ps1 do konta usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="ebd87-110">This command imports the DSC configuration in the file named client.ps1 into the Automation account named Contoso17.</span></span> <span data-ttu-id="ebd87-111">Polecenie określa parametr *Force* .</span><span class="sxs-lookup"><span data-stu-id="ebd87-111">The command specifies the *Force* parameter.</span></span> <span data-ttu-id="ebd87-112">W przypadku istnienia istniejącej konfiguracji DSC to polecenie zastępuje je.</span><span class="sxs-lookup"><span data-stu-id="ebd87-112">If there is an existing DSC configuration, this command replaces it.</span></span>

## <span data-ttu-id="ebd87-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ebd87-113">PARAMETERS</span></span>

### <span data-ttu-id="ebd87-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ebd87-114">-AutomationAccountName</span></span>
<span data-ttu-id="ebd87-115">Określa nazwę konta automatyzacji, do którego to polecenie cmdlet importuje konfigurację DSC.</span><span class="sxs-lookup"><span data-stu-id="ebd87-115">Specifies the name of the Automation account into which this cmdlet imports a DSC configuration.</span></span>

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

### <span data-ttu-id="ebd87-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebd87-116">-DefaultProfile</span></span>
<span data-ttu-id="ebd87-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="ebd87-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ebd87-118">— Opis</span><span class="sxs-lookup"><span data-stu-id="ebd87-118">-Description</span></span>
<span data-ttu-id="ebd87-119">Określa opis konfiguracji zaimportowanej za pomocą tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ebd87-119">Specifies a description of the configuration that this cmdlet imports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebd87-120">-Force</span><span class="sxs-lookup"><span data-stu-id="ebd87-120">-Force</span></span>
<span data-ttu-id="ebd87-121">Wskazuje, że to polecenie cmdlet zastępuje istniejącą konfigurację DSC w automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="ebd87-121">Indicates that this cmdlet replaces an existing DSC configuration in Automation.</span></span>

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

### <span data-ttu-id="ebd87-122">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="ebd87-122">-LogVerbose</span></span>
<span data-ttu-id="ebd87-123">Określa, czy to polecenie cmdlet ma włączać i wyłączać pełne rejestrowanie w zadaniach kompilacji tej konfiguracji DSC.</span><span class="sxs-lookup"><span data-stu-id="ebd87-123">Specifies whether this cmdlet turns verbose logging on or off for compilation jobs of this DSC configuration.</span></span> <span data-ttu-id="ebd87-124">Określ wartość $True, aby włączyć $False lub wyłączyć pełne logowanie w celu jego wyłączenia.</span><span class="sxs-lookup"><span data-stu-id="ebd87-124">Specify a value of $True to turn verbose logging on or $False to turn it off.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebd87-125">-Opublikowano</span><span class="sxs-lookup"><span data-stu-id="ebd87-125">-Published</span></span>
<span data-ttu-id="ebd87-126">Wskazuje, że to polecenie cmdlet zaimportuje konfigurację DSC w opublikowanym stanie.</span><span class="sxs-lookup"><span data-stu-id="ebd87-126">Indicates that this cmdlet imports the DSC configuration in the published state.</span></span>

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

### <span data-ttu-id="ebd87-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebd87-127">-ResourceGroupName</span></span>
<span data-ttu-id="ebd87-128">Określa nazwę grupy zasobów, dla której to polecenie cmdlet zaimportuje konfigurację DSC.</span><span class="sxs-lookup"><span data-stu-id="ebd87-128">Specifies the name of a resource group for which this cmdlet imports a DSC configuration.</span></span>

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

### <span data-ttu-id="ebd87-129">-SourcePath</span><span class="sxs-lookup"><span data-stu-id="ebd87-129">-SourcePath</span></span>
<span data-ttu-id="ebd87-130">Określa ścieżkę wps_2 skryptu zawierającego konfigurację DSC zaimportowaną przez ten polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ebd87-130">Specifies the path of the wps_2 script that contains the DSC configuration that this cmdlet imports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Path

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebd87-131">-Tagi</span><span class="sxs-lookup"><span data-stu-id="ebd87-131">-Tags</span></span>
<span data-ttu-id="ebd87-132">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="ebd87-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ebd87-133">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="ebd87-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebd87-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ebd87-134">-Confirm</span></span>
<span data-ttu-id="ebd87-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ebd87-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ebd87-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ebd87-136">-WhatIf</span></span>
<span data-ttu-id="ebd87-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ebd87-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ebd87-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ebd87-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ebd87-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebd87-139">CommonParameters</span></span>
<span data-ttu-id="ebd87-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ebd87-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebd87-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebd87-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebd87-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ebd87-142">INPUTS</span></span>

### <span data-ttu-id="ebd87-143">System. String</span><span class="sxs-lookup"><span data-stu-id="ebd87-143">System.String</span></span>

### <span data-ttu-id="ebd87-144">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="ebd87-144">System.Collections.IDictionary</span></span>

### <span data-ttu-id="ebd87-145">System. Nullable "1 [[System. Boolean, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ebd87-145">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="ebd87-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ebd87-146">OUTPUTS</span></span>

### <span data-ttu-id="ebd87-147">Microsoft. Azure. Commands. Automation. model. DscConfiguration</span><span class="sxs-lookup"><span data-stu-id="ebd87-147">Microsoft.Azure.Commands.Automation.Model.DscConfiguration</span></span>

## <span data-ttu-id="ebd87-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ebd87-148">NOTES</span></span>

## <span data-ttu-id="ebd87-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ebd87-149">RELATED LINKS</span></span>

[<span data-ttu-id="ebd87-150">Eksportowanie — AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="ebd87-150">Export-AzAutomationDscConfiguration</span></span>](./Export-AzAutomationDscConfiguration.md)

[<span data-ttu-id="ebd87-151">Get-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="ebd87-151">Get-AzAutomationDscConfiguration</span></span>](./Get-AzAutomationDscConfiguration.md)
