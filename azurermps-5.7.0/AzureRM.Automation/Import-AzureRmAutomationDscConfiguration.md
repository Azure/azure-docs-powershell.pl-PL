---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: BA508F0B-847F-4531-9D5D-A5A044A2D207
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/import-azurermautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRmAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRmAutomationDscConfiguration.md
ms.openlocfilehash: e8d7cfcf595d7dd445d66865d922676c96b7e6d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525374"
---
# <span data-ttu-id="f781a-101">Import-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="f781a-101">Import-AzureRmAutomationDscConfiguration</span></span>

## <span data-ttu-id="f781a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f781a-102">SYNOPSIS</span></span>
<span data-ttu-id="f781a-103">Importuje konfigurację DSC do automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="f781a-103">Imports a DSC configuration into Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f781a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f781a-104">SYNTAX</span></span>

```
Import-AzureRmAutomationDscConfiguration -SourcePath <String> [-Tags <IDictionary>] [-Description <String>]
 [-Published] [-Force] [-LogVerbose <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f781a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f781a-105">DESCRIPTION</span></span>
<span data-ttu-id="f781a-106">Polecenie cmdlet **Import-AzureRmAutomationDscConfiguration** importuje konfigurację konfiguracji pożądanego stanu (DSC) do usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="f781a-106">The **Import-AzureRmAutomationDscConfiguration** cmdlet imports an APS Desired State Configuration (DSC) configuration into Azure Automation.</span></span>
<span data-ttu-id="f781a-107">Określ ścieżkę do skryptu APS, który zawiera jedną konfigurację DSC.</span><span class="sxs-lookup"><span data-stu-id="f781a-107">Specify the path of an APS script that contains a single DSC configuration.</span></span>

## <span data-ttu-id="f781a-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f781a-108">EXAMPLES</span></span>

### <span data-ttu-id="f781a-109">Przykład 1: Importowanie konfiguracji DSC do automatyzacji</span><span class="sxs-lookup"><span data-stu-id="f781a-109">Example 1: Import a DSC configuration into Automation</span></span>
```
PS C:\>Import-AzureRmAutomationDscConfiguration -AutomationAccountName "Contoso17"-ResourceGroupName "ResourceGroup01" -SourcePath "C:\DSC\client.ps1" -Force
```

<span data-ttu-id="f781a-110">To polecenie powoduje zaimportowanie konfiguracji DSC z pliku o nazwie client.ps1 do konta usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="f781a-110">This command imports the DSC configuration in the file named client.ps1 into the Automation account named Contoso17.</span></span> <span data-ttu-id="f781a-111">Polecenie określa parametr *Force* .</span><span class="sxs-lookup"><span data-stu-id="f781a-111">The command specifies the *Force* parameter.</span></span> <span data-ttu-id="f781a-112">W przypadku istnienia istniejącej konfiguracji DSC to polecenie zastępuje je.</span><span class="sxs-lookup"><span data-stu-id="f781a-112">If there is an existing DSC configuration, this command replaces it.</span></span>

## <span data-ttu-id="f781a-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f781a-113">PARAMETERS</span></span>

### <span data-ttu-id="f781a-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f781a-114">-AutomationAccountName</span></span>
<span data-ttu-id="f781a-115">Określa nazwę konta automatyzacji, do którego to polecenie cmdlet importuje konfigurację DSC.</span><span class="sxs-lookup"><span data-stu-id="f781a-115">Specifies the name of the Automation account into which this cmdlet imports a DSC configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f781a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f781a-116">-DefaultProfile</span></span>
<span data-ttu-id="f781a-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="f781a-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f781a-118">— Opis</span><span class="sxs-lookup"><span data-stu-id="f781a-118">-Description</span></span>
<span data-ttu-id="f781a-119">Określa opis konfiguracji zaimportowanej za pomocą tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f781a-119">Specifies a description of the configuration that this cmdlet imports.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f781a-120">-Force</span><span class="sxs-lookup"><span data-stu-id="f781a-120">-Force</span></span>
<span data-ttu-id="f781a-121">Wskazuje, że to polecenie cmdlet zastępuje istniejącą konfigurację DSC w automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="f781a-121">Indicates that this cmdlet replaces an existing DSC configuration in Automation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f781a-122">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="f781a-122">-LogVerbose</span></span>
<span data-ttu-id="f781a-123">Określa, czy to polecenie cmdlet ma włączać i wyłączać pełne rejestrowanie w zadaniach kompilacji tej konfiguracji DSC.</span><span class="sxs-lookup"><span data-stu-id="f781a-123">Specifies whether this cmdlet turns verbose logging on or off for compilation jobs of this DSC configuration.</span></span> <span data-ttu-id="f781a-124">Określ wartość $True, aby włączyć $False lub wyłączyć pełne logowanie w celu jego wyłączenia.</span><span class="sxs-lookup"><span data-stu-id="f781a-124">Specify a value of $True to turn verbose logging on or $False to turn it off.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f781a-125">-Opublikowano</span><span class="sxs-lookup"><span data-stu-id="f781a-125">-Published</span></span>
<span data-ttu-id="f781a-126">Wskazuje, że to polecenie cmdlet zaimportuje konfigurację DSC w opublikowanym stanie.</span><span class="sxs-lookup"><span data-stu-id="f781a-126">Indicates that this cmdlet imports the DSC configuration in the published state.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f781a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f781a-127">-ResourceGroupName</span></span>
<span data-ttu-id="f781a-128">Określa nazwę grupy zasobów, dla której to polecenie cmdlet zaimportuje konfigurację DSC.</span><span class="sxs-lookup"><span data-stu-id="f781a-128">Specifies the name of a resource group for which this cmdlet imports a DSC configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f781a-129">-SourcePath</span><span class="sxs-lookup"><span data-stu-id="f781a-129">-SourcePath</span></span>
<span data-ttu-id="f781a-130">Określa ścieżkę wps_2 skryptu zawierającego konfigurację DSC zaimportowaną przez ten polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f781a-130">Specifies the path of the wps_2 script that contains the DSC configuration that this cmdlet imports.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Path

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f781a-131">-Tagi</span><span class="sxs-lookup"><span data-stu-id="f781a-131">-Tags</span></span>
<span data-ttu-id="f781a-132">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="f781a-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f781a-133">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="f781a-133">For example:</span></span>

<span data-ttu-id="f781a-134">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="f781a-134">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f781a-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f781a-135">-Confirm</span></span>
<span data-ttu-id="f781a-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f781a-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f781a-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f781a-137">-WhatIf</span></span>
<span data-ttu-id="f781a-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f781a-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f781a-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f781a-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f781a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f781a-140">CommonParameters</span></span>
<span data-ttu-id="f781a-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f781a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f781a-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f781a-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f781a-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f781a-143">INPUTS</span></span>

### <span data-ttu-id="f781a-144">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="f781a-144">None</span></span>
<span data-ttu-id="f781a-145">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="f781a-145">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f781a-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f781a-146">OUTPUTS</span></span>

### <span data-ttu-id="f781a-147">Microsoft. Azure. Commands. Automation. model. DscConfiguration</span><span class="sxs-lookup"><span data-stu-id="f781a-147">Microsoft.Azure.Commands.Automation.Model.DscConfiguration</span></span>

## <span data-ttu-id="f781a-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f781a-148">NOTES</span></span>

## <span data-ttu-id="f781a-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f781a-149">RELATED LINKS</span></span>

[<span data-ttu-id="f781a-150">Eksportowanie — AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="f781a-150">Export-AzureRmAutomationDscConfiguration</span></span>](./Export-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="f781a-151">Get-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="f781a-151">Get-AzureRmAutomationDscConfiguration</span></span>](./Get-AzureRmAutomationDscConfiguration.md)
