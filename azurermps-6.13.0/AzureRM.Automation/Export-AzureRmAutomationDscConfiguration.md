---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 595D3304-3331-4F44-BA57-AE090FB8A132
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/export-azurermautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRmAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRmAutomationDscConfiguration.md
ms.openlocfilehash: f690e5d7e35b819b727e2ea3f12c8f5e0b2a375f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524674"
---
# <span data-ttu-id="3627f-101">Export-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="3627f-101">Export-AzureRmAutomationDscConfiguration</span></span>

## <span data-ttu-id="3627f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3627f-102">SYNOPSIS</span></span>
<span data-ttu-id="3627f-103">Umożliwia wyeksportowanie konfiguracji DSC z automatyzacji do pliku lokalnego.</span><span class="sxs-lookup"><span data-stu-id="3627f-103">Exports a DSC configuration from Automation to a local file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3627f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3627f-104">SYNTAX</span></span>

```
Export-AzureRmAutomationDscConfiguration -Name <String> [-Slot <String>] [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3627f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3627f-105">DESCRIPTION</span></span>
<span data-ttu-id="3627f-106">Polecenie cmdlet **Export-AzureRmAutomationDscConfiguration** umożliwia wyeksportowanie konfiguracji programu APS (żądana konfiguracja) z usługi Azure Automation do pliku lokalnego.</span><span class="sxs-lookup"><span data-stu-id="3627f-106">The **Export-AzureRmAutomationDscConfiguration** cmdlet exports an APS Desired State Configuration (DSC) configuration from Azure Automation to a local file.</span></span>
<span data-ttu-id="3627f-107">Wyeksportowany plik ma rozszerzenie nazwy pliku ps1.</span><span class="sxs-lookup"><span data-stu-id="3627f-107">The exported file has a .ps1 file name extension.</span></span>

## <span data-ttu-id="3627f-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3627f-108">EXAMPLES</span></span>

### <span data-ttu-id="3627f-109">Przykład 1. Eksportowanie opublikowanej wersji konfiguracji DSC</span><span class="sxs-lookup"><span data-stu-id="3627f-109">Example 1: Export the published version of a DSC configuration</span></span>
```
PS C:\>Export-AzureRmAutomationDscConfiguration -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Name "Configuration01" -Slot Published -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="3627f-110">To polecenie eksportuje opublikowaną wersję konfiguracji DSC w aplikacji Automation do określonego folderu, który jest pulpitem.</span><span class="sxs-lookup"><span data-stu-id="3627f-110">This command exports the published version of a DSC configuration in Automation to the specified folder, which is the desktop.</span></span>

## <span data-ttu-id="3627f-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3627f-111">PARAMETERS</span></span>

### <span data-ttu-id="3627f-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3627f-112">-AutomationAccountName</span></span>
<span data-ttu-id="3627f-113">Określa nazwę konta automatyzacji zawierającego DSC, które jest eksportowane za pomocą tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3627f-113">Specifies the name of the Automation account that contains the DSC that this cmdlet exports.</span></span>

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

### <span data-ttu-id="3627f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3627f-114">-DefaultProfile</span></span>
<span data-ttu-id="3627f-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="3627f-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3627f-116">-Force</span><span class="sxs-lookup"><span data-stu-id="3627f-116">-Force</span></span>
<span data-ttu-id="3627f-117">Wskazuje, że to polecenie cmdlet Zamienia istniejący plik lokalny na nowy plik o tej samej nazwie.</span><span class="sxs-lookup"><span data-stu-id="3627f-117">Indicates that this cmdlet replaces an existing local file with a new file that has the same name.</span></span>

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

### <span data-ttu-id="3627f-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3627f-118">-Name</span></span>
<span data-ttu-id="3627f-119">Określa nazwę konfiguracji DSC wyeksportowanej przez polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3627f-119">Specifies the name of the DSC configuration that this cmdlet exports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3627f-120">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="3627f-120">-OutputFolder</span></span>
<span data-ttu-id="3627f-121">Określa folder wyjściowy, w którym ten aplet polecenia wyeksportuje konfigurację DSC.</span><span class="sxs-lookup"><span data-stu-id="3627f-121">Specifies the output folder where this cmdlet exports the DSC configuration.</span></span>

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

### <span data-ttu-id="3627f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3627f-122">-ResourceGroupName</span></span>
<span data-ttu-id="3627f-123">Określa nazwę grupy zasobów, dla której to polecenie cmdlet eksportuje konfigurację DSC.</span><span class="sxs-lookup"><span data-stu-id="3627f-123">Specifies the name of a resource group for which this cmdlet exports a DSC configuration.</span></span>

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

### <span data-ttu-id="3627f-124">-Slot</span><span class="sxs-lookup"><span data-stu-id="3627f-124">-Slot</span></span>
<span data-ttu-id="3627f-125">Określa wersję konfiguracji DSC wyeksportowanej przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3627f-125">Specifies which version of the DSC configuration that this cmdlet exports.</span></span>
<span data-ttu-id="3627f-126">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="3627f-126">Valid values are:</span></span> 
- <span data-ttu-id="3627f-127">Propozycje</span><span class="sxs-lookup"><span data-stu-id="3627f-127">Draft</span></span>
- <span data-ttu-id="3627f-128">Opublikowano wartość domyślną.</span><span class="sxs-lookup"><span data-stu-id="3627f-128">Published The default value is Published.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Published, Draft

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3627f-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3627f-129">-Confirm</span></span>
<span data-ttu-id="3627f-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3627f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3627f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3627f-131">-WhatIf</span></span>
<span data-ttu-id="3627f-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3627f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3627f-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3627f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3627f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3627f-134">CommonParameters</span></span>
<span data-ttu-id="3627f-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3627f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3627f-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3627f-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3627f-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3627f-137">INPUTS</span></span>

### <span data-ttu-id="3627f-138">System. String</span><span class="sxs-lookup"><span data-stu-id="3627f-138">System.String</span></span>

## <span data-ttu-id="3627f-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3627f-139">OUTPUTS</span></span>

### <span data-ttu-id="3627f-140">System. IO. DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="3627f-140">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="3627f-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3627f-141">NOTES</span></span>

## <span data-ttu-id="3627f-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3627f-142">RELATED LINKS</span></span>

[<span data-ttu-id="3627f-143">Get-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="3627f-143">Get-AzureRmAutomationDscConfiguration</span></span>](./Get-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="3627f-144">Import — AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="3627f-144">Import-AzureRmAutomationDscConfiguration</span></span>](./Import-AzureRmAutomationDscConfiguration.md)


