---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/remove-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayAuthorizationRule.md
ms.openlocfilehash: f99330a7611964e8db3d41f4ece56bb247c1c403
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178931"
---
# <span data-ttu-id="2feaf-101">Remove-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="2feaf-101">Remove-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="2feaf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2feaf-102">SYNOPSIS</span></span>
<span data-ttu-id="2feaf-103">Usuwa regułę autoryzacji połączenia hybrydowego z podanych obiektów przekazywania (Przestrzeń nazw/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="2feaf-103">Removes the authorization rule of a HybridConnection from the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="2feaf-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2feaf-104">SYNTAX</span></span>

### <span data-ttu-id="2feaf-105">NamespaceAuthorizationRuleSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="2feaf-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2feaf-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="2feaf-106">WcfRelayAuthorizationRuleSet</span></span>
```
Remove-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2feaf-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="2feaf-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Remove-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2feaf-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="2feaf-108">DESCRIPTION</span></span>
<span data-ttu-id="2feaf-109">Polecenie **cmdlet Remove-AzRelayAuthorizationRule** usuwa regułę autoryzacji dla danych obiektów przekazywania (Przestrzeń nazw/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="2feaf-109">The **Remove-AzRelayAuthorizationRule** cmdlet removes the authorization rule of the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="2feaf-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2feaf-110">EXAMPLES</span></span>

### <span data-ttu-id="2feaf-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2feaf-111">Example 1</span></span>
```
PS C:\> Remove-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1
```

<span data-ttu-id="2feaf-112">Usuwa regułę autoryzacji `AuthoRule1` przestrzeni `TestNameSpace-Relay1` nazw.</span><span class="sxs-lookup"><span data-stu-id="2feaf-112">Removes the authorization rule `AuthoRule1` of the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="2feaf-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="2feaf-113">Example 2</span></span>
```
PS C:\> Remove-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWcfRelay -Name AuthoRule1
```

<span data-ttu-id="2feaf-114">Usuwa regułę `AuthoRule1` autoryzacji pliku WcfRelay `TestWcfRelay` z przestrzeni `TestNameSpace-Relay1` nazw.</span><span class="sxs-lookup"><span data-stu-id="2feaf-114">Removes the authorization rule `AuthoRule1` of the WcfRelay `TestWcfRelay` from the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="2feaf-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="2feaf-115">Example 3</span></span>
```
PS C:\> Remove-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
```

<span data-ttu-id="2feaf-116">Usuwa regułę `AuthoRule1` autoryzacji połączenia hybrydowego `TestHybridConnection` z przestrzeni `TestNameSpace-Relay1` nazw.</span><span class="sxs-lookup"><span data-stu-id="2feaf-116">Removes the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="2feaf-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2feaf-117">PARAMETERS</span></span>

### <span data-ttu-id="2feaf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2feaf-118">-DefaultProfile</span></span>
<span data-ttu-id="2feaf-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2feaf-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2feaf-120">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="2feaf-120">-Force</span></span>
<span data-ttu-id="2feaf-121">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2feaf-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="2feaf-122">— HybridConnection</span><span class="sxs-lookup"><span data-stu-id="2feaf-122">-HybridConnection</span></span>
<span data-ttu-id="2feaf-123">Nazwa połączenia hybrydowego.</span><span class="sxs-lookup"><span data-stu-id="2feaf-123">HybridConnection Name.</span></span>

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

### <span data-ttu-id="2feaf-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="2feaf-124">-Name</span></span>
<span data-ttu-id="2feaf-125">Nazwa podmiotu autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="2feaf-125">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="2feaf-126">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="2feaf-126">-Namespace</span></span>
<span data-ttu-id="2feaf-127">Nazwa przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="2feaf-127">Namespace Name.</span></span>

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

### <span data-ttu-id="2feaf-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2feaf-128">-PassThru</span></span>
<span data-ttu-id="2feaf-129">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="2feaf-129">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="2feaf-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2feaf-130">-ResourceGroupName</span></span>
<span data-ttu-id="2feaf-131">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2feaf-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="2feaf-132">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="2feaf-132">-WcfRelay</span></span>
<span data-ttu-id="2feaf-133">Nazwa aplikacji WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="2feaf-133">WcfRelay Name.</span></span>

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

### <span data-ttu-id="2feaf-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2feaf-134">-Confirm</span></span>
<span data-ttu-id="2feaf-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2feaf-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2feaf-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2feaf-136">-WhatIf</span></span>
<span data-ttu-id="2feaf-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2feaf-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2feaf-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="2feaf-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2feaf-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2feaf-139">CommonParameters</span></span>
<span data-ttu-id="2feaf-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2feaf-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2feaf-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2feaf-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2feaf-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2feaf-142">INPUTS</span></span>

### <span data-ttu-id="2feaf-143">System.String</span><span class="sxs-lookup"><span data-stu-id="2feaf-143">System.String</span></span>

## <span data-ttu-id="2feaf-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2feaf-144">OUTPUTS</span></span>

### <span data-ttu-id="2feaf-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2feaf-145">System.Boolean</span></span>

## <span data-ttu-id="2feaf-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2feaf-146">NOTES</span></span>

## <span data-ttu-id="2feaf-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2feaf-147">RELATED LINKS</span></span>
