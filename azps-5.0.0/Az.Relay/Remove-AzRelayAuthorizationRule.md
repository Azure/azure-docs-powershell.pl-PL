---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/remove-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayAuthorizationRule.md
ms.openlocfilehash: f99330a7611964e8db3d41f4ece56bb247c1c403
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94317766"
---
# <span data-ttu-id="6e9a5-101">Remove-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="6e9a5-101">Remove-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="6e9a5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6e9a5-102">SYNOPSIS</span></span>
<span data-ttu-id="6e9a5-103">Usuwa regułę autoryzacji HybridConnection z danych jednostek przekazujących (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="6e9a5-103">Removes the authorization rule of a HybridConnection from the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="6e9a5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6e9a5-104">SYNTAX</span></span>

### <span data-ttu-id="6e9a5-105">NamespaceAuthorizationRuleSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6e9a5-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e9a5-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="6e9a5-106">WcfRelayAuthorizationRuleSet</span></span>
```
Remove-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6e9a5-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="6e9a5-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Remove-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e9a5-108">Opis</span><span class="sxs-lookup"><span data-stu-id="6e9a5-108">DESCRIPTION</span></span>
<span data-ttu-id="6e9a5-109">Polecenie cmdlet **Remove-AzRelayAuthorizationRule** usuwa regułę autoryzacji dla określonych jednostek przekazujących (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="6e9a5-109">The **Remove-AzRelayAuthorizationRule** cmdlet removes the authorization rule of the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="6e9a5-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6e9a5-110">EXAMPLES</span></span>

### <span data-ttu-id="6e9a5-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6e9a5-111">Example 1</span></span>
```
PS C:\> Remove-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1
```

<span data-ttu-id="6e9a5-112">Usuwa regułę autoryzacji `AuthoRule1` obszaru nazw `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="6e9a5-112">Removes the authorization rule `AuthoRule1` of the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="6e9a5-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="6e9a5-113">Example 2</span></span>
```
PS C:\> Remove-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWcfRelay -Name AuthoRule1
```

<span data-ttu-id="6e9a5-114">Usuwa regułę autoryzacji `AuthoRule1` WcfRelay `TestWcfRelay` z obszaru nazw `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="6e9a5-114">Removes the authorization rule `AuthoRule1` of the WcfRelay `TestWcfRelay` from the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="6e9a5-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="6e9a5-115">Example 3</span></span>
```
PS C:\> Remove-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
```

<span data-ttu-id="6e9a5-116">Usuwa regułę autoryzacji `AuthoRule1` HybridConnection `TestHybridConnection` z obszaru nazw `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="6e9a5-116">Removes the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="6e9a5-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6e9a5-117">PARAMETERS</span></span>

### <span data-ttu-id="6e9a5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e9a5-118">-DefaultProfile</span></span>
<span data-ttu-id="6e9a5-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6e9a5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e9a5-120">-Force</span><span class="sxs-lookup"><span data-stu-id="6e9a5-120">-Force</span></span>
<span data-ttu-id="6e9a5-121">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6e9a5-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="6e9a5-122">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="6e9a5-122">-HybridConnection</span></span>
<span data-ttu-id="6e9a5-123">Nazwa HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="6e9a5-123">HybridConnection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: HybridConnectionAuthorizationRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e9a5-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6e9a5-124">-Name</span></span>
<span data-ttu-id="6e9a5-125">Nazwa AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="6e9a5-125">AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e9a5-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="6e9a5-126">-Namespace</span></span>
<span data-ttu-id="6e9a5-127">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="6e9a5-127">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e9a5-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6e9a5-128">-PassThru</span></span>
<span data-ttu-id="6e9a5-129">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="6e9a5-129">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="6e9a5-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e9a5-130">-ResourceGroupName</span></span>
<span data-ttu-id="6e9a5-131">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6e9a5-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="6e9a5-132">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="6e9a5-132">-WcfRelay</span></span>
<span data-ttu-id="6e9a5-133">Nazwa WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="6e9a5-133">WcfRelay Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e9a5-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6e9a5-134">-Confirm</span></span>
<span data-ttu-id="6e9a5-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e9a5-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e9a5-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e9a5-136">-WhatIf</span></span>
<span data-ttu-id="6e9a5-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e9a5-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e9a5-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6e9a5-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e9a5-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e9a5-139">CommonParameters</span></span>
<span data-ttu-id="6e9a5-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e9a5-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e9a5-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e9a5-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e9a5-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6e9a5-142">INPUTS</span></span>

### <span data-ttu-id="6e9a5-143">System. String</span><span class="sxs-lookup"><span data-stu-id="6e9a5-143">System.String</span></span>

## <span data-ttu-id="6e9a5-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6e9a5-144">OUTPUTS</span></span>

### <span data-ttu-id="6e9a5-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6e9a5-145">System.Boolean</span></span>

## <span data-ttu-id="6e9a5-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6e9a5-146">NOTES</span></span>

## <span data-ttu-id="6e9a5-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6e9a5-147">RELATED LINKS</span></span>
