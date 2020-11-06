---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: EAD39EE1-C66F-4092-8876-E7F9FA612481
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationSchedule.md
ms.openlocfilehash: 562b5b5986d544f5fa8d91e0f39cb34ef9dababd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548387"
---
# <span data-ttu-id="cd993-101">Remove-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="cd993-101">Remove-AzureRmAutomationSchedule</span></span>

## <span data-ttu-id="cd993-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cd993-102">SYNOPSIS</span></span>
<span data-ttu-id="cd993-103">Usuwa harmonogram automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="cd993-103">Deletes an Automation schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd993-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cd993-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationSchedule [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cd993-105">Opis</span><span class="sxs-lookup"><span data-stu-id="cd993-105">DESCRIPTION</span></span>
<span data-ttu-id="cd993-106">Polecenie cmdlet **Remove-AzureRmAutomationSchedule** usuwa harmonogram z usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="cd993-106">The **Remove-AzureRmAutomationSchedule** cmdlet deletes a schedule from Azure Automation.</span></span>

## <span data-ttu-id="cd993-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cd993-107">EXAMPLES</span></span>

### <span data-ttu-id="cd993-108">Przykład 1. Usuń harmonogram</span><span class="sxs-lookup"><span data-stu-id="cd993-108">Example 1: Remove a schedule</span></span>
```
PS C:\>Remove-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="cd993-109">To polecenie modyfikuje opis harmonogramu o nazwie Schedule01.</span><span class="sxs-lookup"><span data-stu-id="cd993-109">This command modifies the description of the schedule named Schedule01.</span></span>

## <span data-ttu-id="cd993-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cd993-110">PARAMETERS</span></span>

### <span data-ttu-id="cd993-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="cd993-111">-AutomationAccountName</span></span>
<span data-ttu-id="cd993-112">Określa nazwę konta automatyzacji, dla którego jest modyfikowany harmonogram za pomocą tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd993-112">Specifies the name of an Automation account for which this cmdlet modifies a schedule.</span></span>

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

### <span data-ttu-id="cd993-113">-Force</span><span class="sxs-lookup"><span data-stu-id="cd993-113">-Force</span></span>
<span data-ttu-id="cd993-114">ps_force</span><span class="sxs-lookup"><span data-stu-id="cd993-114">ps_force</span></span>

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

### <span data-ttu-id="cd993-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cd993-115">-Name</span></span>
<span data-ttu-id="cd993-116">Określa nazwę harmonogramu, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd993-116">Specifies the name for the schedule that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd993-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd993-117">-ResourceGroupName</span></span>
<span data-ttu-id="cd993-118">Określa nazwę grupy zasobów, dla której ten aplet polecenia usunie harmonogram.</span><span class="sxs-lookup"><span data-stu-id="cd993-118">Specifies the name of a resource group for which this cmdlet removes a schedule.</span></span>

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

### <span data-ttu-id="cd993-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cd993-119">-Confirm</span></span>
<span data-ttu-id="cd993-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd993-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd993-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd993-121">-WhatIf</span></span>
<span data-ttu-id="cd993-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd993-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd993-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cd993-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd993-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd993-124">-DefaultProfile</span></span>
<span data-ttu-id="cd993-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cd993-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd993-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd993-126">CommonParameters</span></span>
<span data-ttu-id="cd993-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd993-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd993-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd993-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd993-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cd993-129">INPUTS</span></span>

## <span data-ttu-id="cd993-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cd993-130">OUTPUTS</span></span>

## <span data-ttu-id="cd993-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cd993-131">NOTES</span></span>

## <span data-ttu-id="cd993-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cd993-132">RELATED LINKS</span></span>

[<span data-ttu-id="cd993-133">Get-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="cd993-133">Get-AzureRmAutomationSchedule</span></span>](./Get-AzureRMAutomationSchedule.md)

[<span data-ttu-id="cd993-134">Nowe — AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="cd993-134">New-AzureRmAutomationSchedule</span></span>](./New-AzureRMAutomationSchedule.md)

[<span data-ttu-id="cd993-135">Set-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="cd993-135">Set-AzureRmAutomationSchedule</span></span>](./Set-AzureRMAutomationSchedule.md)


