---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayAuthorizationRule.md
ms.openlocfilehash: 8eaf2ff99fe7f3ea49d73af95eb4482c645be59f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718104"
---
# <span data-ttu-id="cce72-101">Remove-AzureRmRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="cce72-101">Remove-AzureRmRelayAuthorizationRule</span></span>

## <span data-ttu-id="cce72-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cce72-102">SYNOPSIS</span></span>
<span data-ttu-id="cce72-103">Usuwa regułę autoryzacji HybridConnection z danych jednostek przekazujących (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="cce72-103">Removes the authorization rule of a HybridConnection from the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cce72-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cce72-104">SYNTAX</span></span>

### <span data-ttu-id="cce72-105">NamespaceAuthorizationRuleSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="cce72-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cce72-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="cce72-106">WcfRelayAuthorizationRuleSet</span></span>
```
Remove-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cce72-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="cce72-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Remove-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cce72-108">Opis</span><span class="sxs-lookup"><span data-stu-id="cce72-108">DESCRIPTION</span></span>
<span data-ttu-id="cce72-109">Polecenie cmdlet **Remove-AzureRmRelayAuthorizationRule** usuwa regułę autoryzacji dla określonych jednostek przekazujących (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="cce72-109">The **Remove-AzureRmRelayAuthorizationRule** cmdlet removes the authorization rule of the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="cce72-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cce72-110">EXAMPLES</span></span>

### <span data-ttu-id="cce72-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cce72-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1
```

<span data-ttu-id="cce72-112">Usuwa regułę autoryzacji `AuthoRule1` obszaru nazw `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="cce72-112">Removes the authorization rule `AuthoRule1` of the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="cce72-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="cce72-113">Example 2</span></span>
```
PS C:\> Remove-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWcfRelay -Name AuthoRule1
```

<span data-ttu-id="cce72-114">Usuwa regułę autoryzacji `AuthoRule1` WcfRelay `TestWcfRelay` z obszaru nazw `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="cce72-114">Removes the authorization rule `AuthoRule1` of the WcfRelay `TestWcfRelay` from the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="cce72-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="cce72-115">Example 3</span></span>
```
PS C:\> Remove-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
```

<span data-ttu-id="cce72-116">Usuwa regułę autoryzacji `AuthoRule1` HybridConnection `TestHybridConnection` z obszaru nazw `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="cce72-116">Removes the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="cce72-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cce72-117">PARAMETERS</span></span>

### <span data-ttu-id="cce72-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cce72-118">-Confirm</span></span>
<span data-ttu-id="cce72-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cce72-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cce72-120">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="cce72-120">-HybridConnection</span></span>
<span data-ttu-id="cce72-121">Nazwa HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="cce72-121">HybridConnection Name.</span></span>

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

### <span data-ttu-id="cce72-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cce72-122">-Name</span></span>
<span data-ttu-id="cce72-123">Nazwa AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="cce72-123">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="cce72-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="cce72-124">-Namespace</span></span>
<span data-ttu-id="cce72-125">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="cce72-125">Namespace Name.</span></span>

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

### <span data-ttu-id="cce72-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cce72-126">-ResourceGroupName</span></span>
<span data-ttu-id="cce72-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cce72-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="cce72-128">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="cce72-128">-WcfRelay</span></span>
<span data-ttu-id="cce72-129">Nazwa WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="cce72-129">WcfRelay Name.</span></span>

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

### <span data-ttu-id="cce72-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cce72-130">-WhatIf</span></span>
<span data-ttu-id="cce72-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cce72-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cce72-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cce72-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cce72-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cce72-133">-DefaultProfile</span></span>
<span data-ttu-id="cce72-134">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cce72-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cce72-135">-Force</span><span class="sxs-lookup"><span data-stu-id="cce72-135">-Force</span></span>
<span data-ttu-id="cce72-136">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="cce72-136">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="cce72-137">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cce72-137">-PassThru</span></span>
<span data-ttu-id="cce72-138">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="cce72-138">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="cce72-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cce72-139">CommonParameters</span></span>
<span data-ttu-id="cce72-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cce72-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cce72-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cce72-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cce72-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cce72-142">INPUTS</span></span>

### <span data-ttu-id="cce72-143">System. String</span><span class="sxs-lookup"><span data-stu-id="cce72-143">System.String</span></span>

## <span data-ttu-id="cce72-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cce72-144">OUTPUTS</span></span>

### <span data-ttu-id="cce72-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cce72-145">System.Boolean</span></span>

## <span data-ttu-id="cce72-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cce72-146">NOTES</span></span>

## <span data-ttu-id="cce72-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cce72-147">RELATED LINKS</span></span>

