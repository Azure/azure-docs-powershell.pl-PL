---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzAlertRule.md
ms.openlocfilehash: 23b4c81e7c999301ccb535435911a9413ae4ef16
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94049345"
---
# <span data-ttu-id="0f6d0-101">Remove-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="0f6d0-101">Remove-AzAlertRule</span></span>

## <span data-ttu-id="0f6d0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0f6d0-102">SYNOPSIS</span></span>
<span data-ttu-id="0f6d0-103">Usuwa regułę alertu.</span><span class="sxs-lookup"><span data-stu-id="0f6d0-103">Removes an alert rule.</span></span>

## <span data-ttu-id="0f6d0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0f6d0-104">SYNTAX</span></span>

```
Remove-AzAlertRule -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f6d0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0f6d0-105">DESCRIPTION</span></span>
<span data-ttu-id="0f6d0-106">Polecenie cmdlet **Remove-AzAlertRule** umożliwia usunięcie reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="0f6d0-106">The **Remove-AzAlertRule** cmdlet removes an alert rule.</span></span>
<span data-ttu-id="0f6d0-107">Musisz określić nazwę reguły alertu i grupę zasobów, do której jest przypisana.</span><span class="sxs-lookup"><span data-stu-id="0f6d0-107">You must specify the name of the alert rule and the resource group to which it is assigned.</span></span>
<span data-ttu-id="0f6d0-108">To polecenie cmdlet implementuje wzorzec ShouldProcess, tzn. może zażądać potwierdzenia od użytkownika przed faktycznym utworzeniem, zmodyfikowaniem lub usunięciem zasobu.</span><span class="sxs-lookup"><span data-stu-id="0f6d0-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="0f6d0-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0f6d0-109">EXAMPLES</span></span>

### <span data-ttu-id="0f6d0-110">Przykład 1: Usuwanie reguły alertu</span><span class="sxs-lookup"><span data-stu-id="0f6d0-110">Example 1: Remove an alert rule</span></span>
```
PS C:\>Remove-AzAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="0f6d0-111">To polecenie usuwa regułę alertu o nazwie mój alert — 7da64548-214d-42ca-b12b-b245bb8f0ac8 w grupie zasobów domyślne — Centrala internetowa.</span><span class="sxs-lookup"><span data-stu-id="0f6d0-111">This command removes the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 in the resource group Default-Web-CentralUS.</span></span>

## <span data-ttu-id="0f6d0-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0f6d0-112">PARAMETERS</span></span>

### <span data-ttu-id="0f6d0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f6d0-113">-DefaultProfile</span></span>
<span data-ttu-id="0f6d0-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="0f6d0-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0f6d0-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0f6d0-115">-Name</span></span>
<span data-ttu-id="0f6d0-116">Określa nazwę reguły alertu, którą należy usunąć.</span><span class="sxs-lookup"><span data-stu-id="0f6d0-116">Specifies the name of the alert rule to remove.</span></span>

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

### <span data-ttu-id="0f6d0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f6d0-117">-ResourceGroupName</span></span>
<span data-ttu-id="0f6d0-118">Określa nazwę grupy zasobów dla reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="0f6d0-118">Specifies the name of the resource group for the alert rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f6d0-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0f6d0-119">-Confirm</span></span>
<span data-ttu-id="0f6d0-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f6d0-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f6d0-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f6d0-121">-WhatIf</span></span>
<span data-ttu-id="0f6d0-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f6d0-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0f6d0-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0f6d0-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f6d0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f6d0-124">CommonParameters</span></span>
<span data-ttu-id="0f6d0-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f6d0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f6d0-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0f6d0-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f6d0-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0f6d0-127">INPUTS</span></span>

### <span data-ttu-id="0f6d0-128">System. String</span><span class="sxs-lookup"><span data-stu-id="0f6d0-128">System.String</span></span>

## <span data-ttu-id="0f6d0-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0f6d0-129">OUTPUTS</span></span>

### <span data-ttu-id="0f6d0-130">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="0f6d0-130">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="0f6d0-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0f6d0-131">NOTES</span></span>

## <span data-ttu-id="0f6d0-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0f6d0-132">RELATED LINKS</span></span>

[<span data-ttu-id="0f6d0-133">Dodaj-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="0f6d0-133">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="0f6d0-134">Dodaj-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="0f6d0-134">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="0f6d0-135">Get-AzAlertHistory</span><span class="sxs-lookup"><span data-stu-id="0f6d0-135">Get-AzAlertHistory</span></span>](./Get-AzAlertHistory.md)

[<span data-ttu-id="0f6d0-136">Get-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="0f6d0-136">Get-AzAlertRule</span></span>](./Get-AzAlertRule.md)


