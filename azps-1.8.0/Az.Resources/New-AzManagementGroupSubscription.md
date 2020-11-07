---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azmanagementgroupsubscription/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroupSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroupSubscription.md
ms.openlocfilehash: 4fc8e7c7ac4c0339e2334c80ba6750273a844182
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708356"
---
# <span data-ttu-id="bce54-101">New-AzManagementGroupSubscription</span><span class="sxs-lookup"><span data-stu-id="bce54-101">New-AzManagementGroupSubscription</span></span>

## <span data-ttu-id="bce54-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bce54-102">SYNOPSIS</span></span>
<span data-ttu-id="bce54-103">Dodaje subskrypcję do grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="bce54-103">Adds a Subscription to a Management Group.</span></span>

## <span data-ttu-id="bce54-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bce54-104">SYNTAX</span></span>

```
New-AzManagementGroupSubscription [-GroupName] <String> [-SubscriptionId] <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bce54-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bce54-105">DESCRIPTION</span></span>
<span data-ttu-id="bce54-106">Polecenie cmdlet **New-AzManagementGroupSubscription** umożliwia dodanie subskrypcji do grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="bce54-106">The **New-AzManagementGroupSubscription** cmdlet adds a Subscription to a Management Group.</span></span>

## <span data-ttu-id="bce54-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bce54-107">EXAMPLES</span></span>

### <span data-ttu-id="bce54-108">Przykład 1. Dodaj subskrypcję do grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="bce54-108">Example 1: Add Subscription to a Management Group</span></span>
```
PS C:\> New-AzManagementGroupSubscription -GroupName "TestGroup" -SubscriptionId 2120692d-35c3-44c8-81f5-631fa7351726
```

## <span data-ttu-id="bce54-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bce54-109">PARAMETERS</span></span>

### <span data-ttu-id="bce54-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bce54-110">-DefaultProfile</span></span>
<span data-ttu-id="bce54-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bce54-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bce54-112">-GroupName</span><span class="sxs-lookup"><span data-stu-id="bce54-112">-GroupName</span></span>
<span data-ttu-id="bce54-113">Identyfikator grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="bce54-113">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bce54-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bce54-114">-PassThru</span></span>
<span data-ttu-id="bce54-115">Powrót `true` po udanym wykonaniu</span><span class="sxs-lookup"><span data-stu-id="bce54-115">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="bce54-116">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="bce54-116">-SubscriptionId</span></span>
<span data-ttu-id="bce54-117">Identyfikator subskrypcji subskrypcji skojarzonej z zarządzaniem</span><span class="sxs-lookup"><span data-stu-id="bce54-117">Subscription Id of the subscription associated witht the management</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bce54-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bce54-118">-Confirm</span></span>
<span data-ttu-id="bce54-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bce54-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bce54-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bce54-120">-WhatIf</span></span>
<span data-ttu-id="bce54-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bce54-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bce54-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bce54-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bce54-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bce54-123">CommonParameters</span></span>
<span data-ttu-id="bce54-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bce54-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bce54-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bce54-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bce54-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bce54-126">INPUTS</span></span>

### <span data-ttu-id="bce54-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="bce54-127">None</span></span>

## <span data-ttu-id="bce54-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bce54-128">OUTPUTS</span></span>

### <span data-ttu-id="bce54-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bce54-129">System.Boolean</span></span>

## <span data-ttu-id="bce54-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bce54-130">NOTES</span></span>

## <span data-ttu-id="bce54-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bce54-131">RELATED LINKS</span></span>