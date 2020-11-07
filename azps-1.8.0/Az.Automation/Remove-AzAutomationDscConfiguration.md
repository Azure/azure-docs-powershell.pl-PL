---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 6389EE2A-12B5-46A1-A2B9-4B3CF5A55A30
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationDscConfiguration.md
ms.openlocfilehash: 1a556a92d59830a4be331c8415fde0c85ddba539
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710498"
---
# <span data-ttu-id="cfda5-101">Remove-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="cfda5-101">Remove-AzAutomationDscConfiguration</span></span>

## <span data-ttu-id="cfda5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cfda5-102">SYNOPSIS</span></span>
<span data-ttu-id="cfda5-103">Usuwa konfiguracje DSC z automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="cfda5-103">Removes DSC configurations from Automation.</span></span>

## <span data-ttu-id="cfda5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cfda5-104">SYNTAX</span></span>

```
Remove-AzAutomationDscConfiguration [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cfda5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="cfda5-105">DESCRIPTION</span></span>
<span data-ttu-id="cfda5-106">Polecenie cmdlet **Remove-AzAutomationDscConfiguration** usuwa konfiguracje konfiguracji pożądanego stanu (DSC) z usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="cfda5-106">The **Remove-AzAutomationDscConfiguration** cmdlet removes APS Desired State Configuration (DSC) configurations from Azure Automation.</span></span>

## <span data-ttu-id="cfda5-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cfda5-107">EXAMPLES</span></span>

## <span data-ttu-id="cfda5-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cfda5-108">PARAMETERS</span></span>

### <span data-ttu-id="cfda5-109">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="cfda5-109">-AutomationAccountName</span></span>
<span data-ttu-id="cfda5-110">Określa nazwę konta automatyzacji zawierającego konfiguracje DSC, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cfda5-110">Specifies the name of the Automation account that contains DSC configurations that this cmdlet removes.</span></span>

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

### <span data-ttu-id="cfda5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfda5-111">-DefaultProfile</span></span>
<span data-ttu-id="cfda5-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="cfda5-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cfda5-113">-Force</span><span class="sxs-lookup"><span data-stu-id="cfda5-113">-Force</span></span>
<span data-ttu-id="cfda5-114">ps_force</span><span class="sxs-lookup"><span data-stu-id="cfda5-114">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfda5-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cfda5-115">-Name</span></span>
<span data-ttu-id="cfda5-116">Określa nazwę konfiguracji DSC, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cfda5-116">Specifies the name of the DSC configuration that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConfigurationName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfda5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfda5-117">-ResourceGroupName</span></span>
<span data-ttu-id="cfda5-118">Określa nazwę grupy zasobów, dla której to polecenie cmdlet ma pobierać konfigurację DSC.</span><span class="sxs-lookup"><span data-stu-id="cfda5-118">Specifies the name of a resource group for which this cmdlet gets DSC configurations.</span></span>

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

### <span data-ttu-id="cfda5-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cfda5-119">-Confirm</span></span>
<span data-ttu-id="cfda5-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cfda5-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cfda5-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cfda5-121">-WhatIf</span></span>
<span data-ttu-id="cfda5-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cfda5-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cfda5-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cfda5-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cfda5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfda5-124">CommonParameters</span></span>
<span data-ttu-id="cfda5-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfda5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfda5-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfda5-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfda5-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cfda5-127">INPUTS</span></span>

### <span data-ttu-id="cfda5-128">System. String</span><span class="sxs-lookup"><span data-stu-id="cfda5-128">System.String</span></span>

## <span data-ttu-id="cfda5-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cfda5-129">OUTPUTS</span></span>

### <span data-ttu-id="cfda5-130">System. void</span><span class="sxs-lookup"><span data-stu-id="cfda5-130">System.Void</span></span>

## <span data-ttu-id="cfda5-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cfda5-131">NOTES</span></span>

## <span data-ttu-id="cfda5-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cfda5-132">RELATED LINKS</span></span>

[<span data-ttu-id="cfda5-133">Eksportowanie — AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="cfda5-133">Export-AzAutomationDscConfiguration</span></span>](./Export-AzAutomationDscConfiguration.md)

[<span data-ttu-id="cfda5-134">Get-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="cfda5-134">Get-AzAutomationDscConfiguration</span></span>](./Get-AzAutomationDscConfiguration.md)

[<span data-ttu-id="cfda5-135">Import — AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="cfda5-135">Import-AzAutomationDscConfiguration</span></span>](./Import-AzAutomationDscConfiguration.md)


