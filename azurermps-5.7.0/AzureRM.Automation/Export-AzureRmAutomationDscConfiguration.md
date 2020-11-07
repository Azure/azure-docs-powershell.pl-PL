---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 595D3304-3331-4F44-BA57-AE090FB8A132
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/export-azurermautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRmAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRmAutomationDscConfiguration.md
ms.openlocfilehash: 2f739c9471e2a6144c12033ade885a445bade12e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718662"
---
# <span data-ttu-id="9fdc0-101">Export-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="9fdc0-101">Export-AzureRmAutomationDscConfiguration</span></span>

## <span data-ttu-id="9fdc0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9fdc0-102">SYNOPSIS</span></span>
<span data-ttu-id="9fdc0-103">Umożliwia wyeksportowanie konfiguracji DSC z automatyzacji do pliku lokalnego.</span><span class="sxs-lookup"><span data-stu-id="9fdc0-103">Exports a DSC configuration from Automation to a local file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9fdc0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9fdc0-104">SYNTAX</span></span>

```
Export-AzureRmAutomationDscConfiguration -Name <String> [-Slot <String>] [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9fdc0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9fdc0-105">DESCRIPTION</span></span>
<span data-ttu-id="9fdc0-106">Polecenie cmdlet **Export-AzureRmAutomationDscConfiguration** umożliwia wyeksportowanie konfiguracji programu APS (żądana konfiguracja) z usługi Azure Automation do pliku lokalnego.</span><span class="sxs-lookup"><span data-stu-id="9fdc0-106">The **Export-AzureRmAutomationDscConfiguration** cmdlet exports an APS Desired State Configuration (DSC) configuration from Azure Automation to a local file.</span></span>
<span data-ttu-id="9fdc0-107">Wyeksportowany plik ma rozszerzenie nazwy pliku ps1.</span><span class="sxs-lookup"><span data-stu-id="9fdc0-107">The exported file has a .ps1 file name extension.</span></span>

## <span data-ttu-id="9fdc0-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9fdc0-108">EXAMPLES</span></span>

### <span data-ttu-id="9fdc0-109">Przykład 1. Eksportowanie opublikowanej wersji konfiguracji DSC</span><span class="sxs-lookup"><span data-stu-id="9fdc0-109">Example 1: Export the published version of a DSC configuration</span></span>
```
PS C:\>Export-AzureRmAutomationDscConfiguration -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Name "Configuration01" -Slot Published -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="9fdc0-110">To polecenie eksportuje opublikowaną wersję konfiguracji DSC w aplikacji Automation do określonego folderu, który jest pulpitem.</span><span class="sxs-lookup"><span data-stu-id="9fdc0-110">This command exports the published version of a DSC configuration in Automation to the specified folder, which is the desktop.</span></span>

## <span data-ttu-id="9fdc0-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9fdc0-111">PARAMETERS</span></span>

### <span data-ttu-id="9fdc0-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9fdc0-112">-AutomationAccountName</span></span>
<span data-ttu-id="9fdc0-113">Określa nazwę konta automatyzacji zawierającego DSC, które jest eksportowane za pomocą tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9fdc0-113">Specifies the name of the Automation account that contains the DSC that this cmdlet exports.</span></span>

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

### <span data-ttu-id="9fdc0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fdc0-114">-DefaultProfile</span></span>
<span data-ttu-id="9fdc0-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="9fdc0-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9fdc0-116">-Force</span><span class="sxs-lookup"><span data-stu-id="9fdc0-116">-Force</span></span>
<span data-ttu-id="9fdc0-117">Wskazuje, że to polecenie cmdlet Zamienia istniejący plik lokalny na nowy plik o tej samej nazwie.</span><span class="sxs-lookup"><span data-stu-id="9fdc0-117">Indicates that this cmdlet replaces an existing local file with a new file that has the same name.</span></span>

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

### <span data-ttu-id="9fdc0-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9fdc0-118">-Name</span></span>
<span data-ttu-id="9fdc0-119">Określa nazwę konfiguracji DSC wyeksportowanej przez polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9fdc0-119">Specifies the name of the DSC configuration that this cmdlet exports.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fdc0-120">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="9fdc0-120">-OutputFolder</span></span>
<span data-ttu-id="9fdc0-121">Określa folder wyjściowy, w którym ten aplet polecenia wyeksportuje konfigurację DSC.</span><span class="sxs-lookup"><span data-stu-id="9fdc0-121">Specifies the output folder where this cmdlet exports the DSC configuration.</span></span>

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

### <span data-ttu-id="9fdc0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fdc0-122">-ResourceGroupName</span></span>
<span data-ttu-id="9fdc0-123">Określa nazwę grupy zasobów, dla której to polecenie cmdlet eksportuje konfigurację DSC.</span><span class="sxs-lookup"><span data-stu-id="9fdc0-123">Specifies the name of a resource group for which this cmdlet exports a DSC configuration.</span></span>

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

### <span data-ttu-id="9fdc0-124">-Slot</span><span class="sxs-lookup"><span data-stu-id="9fdc0-124">-Slot</span></span>
<span data-ttu-id="9fdc0-125">Określa wersję konfiguracji DSC wyeksportowanej przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9fdc0-125">Specifies which version of the DSC configuration that this cmdlet exports.</span></span>
<span data-ttu-id="9fdc0-126">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="9fdc0-126">Valid values are:</span></span> 

- <span data-ttu-id="9fdc0-127">Propozycje</span><span class="sxs-lookup"><span data-stu-id="9fdc0-127">Draft</span></span>
- <span data-ttu-id="9fdc0-128">Podawane</span><span class="sxs-lookup"><span data-stu-id="9fdc0-128">Published</span></span> 

<span data-ttu-id="9fdc0-129">Wartość domyślna jest publikowana.</span><span class="sxs-lookup"><span data-stu-id="9fdc0-129">The default value is Published.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Published, Draft

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fdc0-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9fdc0-130">-Confirm</span></span>
<span data-ttu-id="9fdc0-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9fdc0-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9fdc0-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fdc0-132">-WhatIf</span></span>
<span data-ttu-id="9fdc0-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9fdc0-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9fdc0-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9fdc0-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9fdc0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fdc0-135">CommonParameters</span></span>
<span data-ttu-id="9fdc0-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fdc0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fdc0-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fdc0-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fdc0-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9fdc0-138">INPUTS</span></span>

### <span data-ttu-id="9fdc0-139">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="9fdc0-139">None</span></span>
<span data-ttu-id="9fdc0-140">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="9fdc0-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9fdc0-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9fdc0-141">OUTPUTS</span></span>

### <span data-ttu-id="9fdc0-142">System. IO. DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="9fdc0-142">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="9fdc0-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9fdc0-143">NOTES</span></span>

## <span data-ttu-id="9fdc0-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9fdc0-144">RELATED LINKS</span></span>

[<span data-ttu-id="9fdc0-145">Get-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="9fdc0-145">Get-AzureRmAutomationDscConfiguration</span></span>](./Get-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="9fdc0-146">Import — AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="9fdc0-146">Import-AzureRmAutomationDscConfiguration</span></span>](./Import-AzureRmAutomationDscConfiguration.md)


