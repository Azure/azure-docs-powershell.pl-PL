---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermmanagementgroupsubscription/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmManagementGroupSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmManagementGroupSubscription.md
ms.openlocfilehash: a3c75c653d75a4fde969672a245644ee04412731
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524281"
---
# <span data-ttu-id="d7d95-101">New-AzureRmManagementGroupSubscription</span><span class="sxs-lookup"><span data-stu-id="d7d95-101">New-AzureRmManagementGroupSubscription</span></span>

## <span data-ttu-id="d7d95-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d7d95-102">SYNOPSIS</span></span>
<span data-ttu-id="d7d95-103">Dodaje subskrypcję do grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="d7d95-103">Adds a Subscription to a Management Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7d95-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d7d95-104">SYNTAX</span></span>

```
New-AzureRmManagementGroupSubscription [-GroupName] <String> [-SubscriptionId] <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7d95-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d7d95-105">DESCRIPTION</span></span>
<span data-ttu-id="d7d95-106">Polecenie cmdlet **New-AzureRMManagementGroupSubscription** umożliwia dodanie subskrypcji do grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="d7d95-106">The **New-AzureRMManagementGroupSubscription** cmdlet adds a Subscription to a Management Group.</span></span>

## <span data-ttu-id="d7d95-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d7d95-107">EXAMPLES</span></span>

### <span data-ttu-id="d7d95-108">Przykład 1. Dodaj subskrypcję do grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="d7d95-108">Example 1: Add Subscription to a Management Group</span></span>
```
PS C:\> New-AzureRMManagementGroupSubscription -GroupName "TestGroup" -SubscriptionId 2120692d-35c3-44c8-81f5-631fa7351726
```

## <span data-ttu-id="d7d95-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d7d95-109">PARAMETERS</span></span>

### <span data-ttu-id="d7d95-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7d95-110">-DefaultProfile</span></span>
<span data-ttu-id="d7d95-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d7d95-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7d95-112">-GroupName</span><span class="sxs-lookup"><span data-stu-id="d7d95-112">-GroupName</span></span>
<span data-ttu-id="d7d95-113">Identyfikator grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="d7d95-113">Management Group Id</span></span>

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

### <span data-ttu-id="d7d95-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d7d95-114">-PassThru</span></span>
<span data-ttu-id="d7d95-115">Powrót `true` po udanym wykonaniu</span><span class="sxs-lookup"><span data-stu-id="d7d95-115">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="d7d95-116">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="d7d95-116">-SubscriptionId</span></span>
<span data-ttu-id="d7d95-117">Identyfikator subskrypcji subskrypcji skojarzonej z zarządzaniem</span><span class="sxs-lookup"><span data-stu-id="d7d95-117">Subscription Id of the subscription associated witht the management</span></span>

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

### <span data-ttu-id="d7d95-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d7d95-118">-Confirm</span></span>
<span data-ttu-id="d7d95-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7d95-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7d95-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7d95-120">-WhatIf</span></span>
<span data-ttu-id="d7d95-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7d95-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7d95-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d7d95-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7d95-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7d95-123">CommonParameters</span></span>
<span data-ttu-id="d7d95-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7d95-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7d95-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7d95-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7d95-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d7d95-126">INPUTS</span></span>

### <span data-ttu-id="d7d95-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="d7d95-127">None</span></span>

## <span data-ttu-id="d7d95-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d7d95-128">OUTPUTS</span></span>

### <span data-ttu-id="d7d95-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d7d95-129">System.Boolean</span></span>

## <span data-ttu-id="d7d95-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d7d95-130">NOTES</span></span>

## <span data-ttu-id="d7d95-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d7d95-131">RELATED LINKS</span></span>
