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
ms.locfileid: "93706729"
---
# <span data-ttu-id="3c971-101">Remove-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="3c971-101">Remove-AzAutomationDscConfiguration</span></span>

## <span data-ttu-id="3c971-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3c971-102">SYNOPSIS</span></span>
<span data-ttu-id="3c971-103">Usuwa konfiguracje DSC z automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="3c971-103">Removes DSC configurations from Automation.</span></span>

## <span data-ttu-id="3c971-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3c971-104">SYNTAX</span></span>

```
Remove-AzAutomationDscConfiguration [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3c971-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3c971-105">DESCRIPTION</span></span>
<span data-ttu-id="3c971-106">Polecenie cmdlet **Remove-AzAutomationDscConfiguration** usuwa konfiguracje konfiguracji pożądanego stanu (DSC) z usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="3c971-106">The **Remove-AzAutomationDscConfiguration** cmdlet removes APS Desired State Configuration (DSC) configurations from Azure Automation.</span></span>

## <span data-ttu-id="3c971-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3c971-107">EXAMPLES</span></span>

## <span data-ttu-id="3c971-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3c971-108">PARAMETERS</span></span>

### <span data-ttu-id="3c971-109">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3c971-109">-AutomationAccountName</span></span>
<span data-ttu-id="3c971-110">Określa nazwę konta automatyzacji zawierającego konfiguracje DSC, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c971-110">Specifies the name of the Automation account that contains DSC configurations that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3c971-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c971-111">-DefaultProfile</span></span>
<span data-ttu-id="3c971-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="3c971-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3c971-113">-Force</span><span class="sxs-lookup"><span data-stu-id="3c971-113">-Force</span></span>
<span data-ttu-id="3c971-114">ps_force</span><span class="sxs-lookup"><span data-stu-id="3c971-114">ps_force</span></span>

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

### <span data-ttu-id="3c971-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3c971-115">-Name</span></span>
<span data-ttu-id="3c971-116">Określa nazwę konfiguracji DSC, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c971-116">Specifies the name of the DSC configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3c971-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c971-117">-ResourceGroupName</span></span>
<span data-ttu-id="3c971-118">Określa nazwę grupy zasobów, dla której to polecenie cmdlet ma pobierać konfigurację DSC.</span><span class="sxs-lookup"><span data-stu-id="3c971-118">Specifies the name of a resource group for which this cmdlet gets DSC configurations.</span></span>

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

### <span data-ttu-id="3c971-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3c971-119">-Confirm</span></span>
<span data-ttu-id="3c971-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c971-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c971-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c971-121">-WhatIf</span></span>
<span data-ttu-id="3c971-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c971-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c971-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3c971-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c971-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c971-124">CommonParameters</span></span>
<span data-ttu-id="3c971-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c971-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c971-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c971-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c971-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3c971-127">INPUTS</span></span>

### <span data-ttu-id="3c971-128">System. String</span><span class="sxs-lookup"><span data-stu-id="3c971-128">System.String</span></span>

## <span data-ttu-id="3c971-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3c971-129">OUTPUTS</span></span>

### <span data-ttu-id="3c971-130">System. void</span><span class="sxs-lookup"><span data-stu-id="3c971-130">System.Void</span></span>

## <span data-ttu-id="3c971-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3c971-131">NOTES</span></span>

## <span data-ttu-id="3c971-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3c971-132">RELATED LINKS</span></span>

[<span data-ttu-id="3c971-133">Eksportowanie — AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="3c971-133">Export-AzAutomationDscConfiguration</span></span>](./Export-AzAutomationDscConfiguration.md)

[<span data-ttu-id="3c971-134">Get-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="3c971-134">Get-AzAutomationDscConfiguration</span></span>](./Get-AzAutomationDscConfiguration.md)

[<span data-ttu-id="3c971-135">Import — AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="3c971-135">Import-AzAutomationDscConfiguration</span></span>](./Import-AzAutomationDscConfiguration.md)


