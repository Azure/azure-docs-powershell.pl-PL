---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagementgroupsubscription/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupSubscription.md
ms.openlocfilehash: a193312379aee69e0256975681ab8eb867e41c8e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871763"
---
# <span data-ttu-id="a677d-101">Remove-AzManagementGroupSubscription</span><span class="sxs-lookup"><span data-stu-id="a677d-101">Remove-AzManagementGroupSubscription</span></span>

## <span data-ttu-id="a677d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a677d-102">SYNOPSIS</span></span>
<span data-ttu-id="a677d-103">Usuwa abonament z grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="a677d-103">Removes a Subscription from a Management Group.</span></span>

## <span data-ttu-id="a677d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a677d-104">SYNTAX</span></span>

```
Remove-AzManagementGroupSubscription [-GroupName] <String> [-SubscriptionId] <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a677d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a677d-105">DESCRIPTION</span></span>
<span data-ttu-id="a677d-106">Polecenie cmdlet **Remove-AzManagementGroupSubscription** usuwa abonament z grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="a677d-106">The **Remove-AzManagementGroupSubscription** cmdlet removes a Subscription from a Management Group.</span></span>

## <span data-ttu-id="a677d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a677d-107">EXAMPLES</span></span>

### <span data-ttu-id="a677d-108">Przykład 1-usuwanie subskrypcji z grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="a677d-108">Example 1 - Remove Subscription from a Management Group</span></span>
```
PS C:\> Remove-AzManagementGroupSubscription -GroupName "TestGroup" -SubscriptionId 2120692d-35c3-44c8-81f5-631fa7351726
```

## <span data-ttu-id="a677d-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a677d-109">PARAMETERS</span></span>

### <span data-ttu-id="a677d-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a677d-110">-DefaultProfile</span></span>
<span data-ttu-id="a677d-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a677d-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a677d-112">-GroupName</span><span class="sxs-lookup"><span data-stu-id="a677d-112">-GroupName</span></span>
<span data-ttu-id="a677d-113">Identyfikator grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="a677d-113">Management Group Id</span></span>

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

### <span data-ttu-id="a677d-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a677d-114">-PassThru</span></span>
<span data-ttu-id="a677d-115">Powrót `true` po udanym wykonaniu</span><span class="sxs-lookup"><span data-stu-id="a677d-115">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="a677d-116">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="a677d-116">-SubscriptionId</span></span>
<span data-ttu-id="a677d-117">Identyfikator subskrypcji subskrypcji skojarzonej z zarządzaniem</span><span class="sxs-lookup"><span data-stu-id="a677d-117">Subscription Id of the subscription associated with the management</span></span>

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

### <span data-ttu-id="a677d-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a677d-118">-Confirm</span></span>
<span data-ttu-id="a677d-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a677d-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a677d-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a677d-120">-WhatIf</span></span>
<span data-ttu-id="a677d-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a677d-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a677d-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a677d-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a677d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a677d-123">CommonParameters</span></span>
<span data-ttu-id="a677d-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a677d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a677d-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a677d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a677d-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a677d-126">INPUTS</span></span>

### <span data-ttu-id="a677d-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="a677d-127">None</span></span>

## <span data-ttu-id="a677d-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a677d-128">OUTPUTS</span></span>

### <span data-ttu-id="a677d-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a677d-129">System.Boolean</span></span>

## <span data-ttu-id="a677d-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a677d-130">NOTES</span></span>

## <span data-ttu-id="a677d-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a677d-131">RELATED LINKS</span></span>
