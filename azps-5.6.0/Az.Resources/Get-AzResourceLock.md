---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 3FBF91B8-8EF9-4E05-AD7E-AEFC6EBBFB8E
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceLock.md
ms.openlocfilehash: 70c52508bbb152047d40d7556a41ad76e3ca2eac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963777"
---
# <span data-ttu-id="46461-101">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="46461-101">Get-AzResourceLock</span></span>

## <span data-ttu-id="46461-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46461-102">SYNOPSIS</span></span>
<span data-ttu-id="46461-103">Uzyskuje blokadę zasobów.</span><span class="sxs-lookup"><span data-stu-id="46461-103">Gets a resource lock.</span></span>

## <span data-ttu-id="46461-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="46461-104">SYNTAX</span></span>

### <span data-ttu-id="46461-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="46461-105">ByResourceGroup</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46461-106">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="46461-106">ByResourceGroupLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="46461-107">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="46461-107">BySpecifiedScope</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46461-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="46461-108">BySubscription</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46461-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="46461-109">BySubscriptionLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46461-110">ByLockId</span><span class="sxs-lookup"><span data-stu-id="46461-110">ByLockId</span></span>
```
Get-AzResourceLock [-AtScope] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46461-111">OPIS</span><span class="sxs-lookup"><span data-stu-id="46461-111">DESCRIPTION</span></span>
<span data-ttu-id="46461-112">Polecenie **cmdlet Get-AzResourceLock** pobiera blokady zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="46461-112">The **Get-AzResourceLock** cmdlet gets Azure resource locks.</span></span>

## <span data-ttu-id="46461-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="46461-113">EXAMPLES</span></span>

### <span data-ttu-id="46461-114">Przykład 1. Uzyskiwanie blokady</span><span class="sxs-lookup"><span data-stu-id="46461-114">Example 1: Get a lock</span></span>
```
PS C:\>Get-AzResourceLock -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="46461-115">To polecenie pobiera blokadę zasobów o nazwie ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="46461-115">This command gets the resource lock named ContosoSiteLock.</span></span>

### <span data-ttu-id="46461-116">Przykład 2. Uzyskiwanie blokad na poziomie grupy zasobów lub wyższej</span><span class="sxs-lookup"><span data-stu-id="46461-116">Example 2: Get locks at resource group level or higher</span></span>
```
PS C:\> Get-AzResourceLock -ResourceGroupName "ResourceGroup11" -AtScope
```

<span data-ttu-id="46461-117">To polecenie pobiera blokady zasobów dla grupy zasobów lub subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="46461-117">This command gets the resource locks on the resource group or the subscription.</span></span>

## <span data-ttu-id="46461-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="46461-118">PARAMETERS</span></span>

### <span data-ttu-id="46461-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="46461-119">-ApiVersion</span></span>
<span data-ttu-id="46461-120">Określa wersję interfejsu API dostawcy zasobów do użycia.</span><span class="sxs-lookup"><span data-stu-id="46461-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="46461-121">Jeśli nie określisz wersji, to polecenie cmdlet użyje najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="46461-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46461-122">-AtScope</span><span class="sxs-lookup"><span data-stu-id="46461-122">-AtScope</span></span>
<span data-ttu-id="46461-123">Wskazuje, że to polecenie cmdlet zwraca wszystkie blokady w określonym zakresie lub powyżej tego zakresu.</span><span class="sxs-lookup"><span data-stu-id="46461-123">Indicates that this cmdlet returns all locks at or above the specified scope.</span></span>
<span data-ttu-id="46461-124">Jeśli nie określisz tego parametru, polecenie cmdlet zwróci wszystkie blokady w zakresie, powyżej lub poniżej tego zakresu.</span><span class="sxs-lookup"><span data-stu-id="46461-124">If you do not specify this parameter, the cmdlet returns all locks at, above, or below the scope.</span></span>

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

### <span data-ttu-id="46461-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46461-125">-DefaultProfile</span></span>
<span data-ttu-id="46461-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="46461-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="46461-127">- LockId</span><span class="sxs-lookup"><span data-stu-id="46461-127">-LockId</span></span>
<span data-ttu-id="46461-128">Określa identyfikator blokady, która będzie owana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46461-128">Specifies the ID of the lock that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByLockId
Aliases: Id, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46461-129">-LockName</span><span class="sxs-lookup"><span data-stu-id="46461-129">-LockName</span></span>
<span data-ttu-id="46461-130">Określa nazwę blokady, do która ma trafiać to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46461-130">Specifies the name of the lock that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel, BySpecifiedScope, BySubscription, BySubscriptionLevel
Aliases: ExtensionResourceName, Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46461-131">— Przed</span><span class="sxs-lookup"><span data-stu-id="46461-131">-Pre</span></span>
<span data-ttu-id="46461-132">Wskazuje, że to polecenie cmdlet uwzględnia wersje przedpremierowe interfejsu API, gdy automatycznie określa, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="46461-132">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="46461-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46461-133">-ResourceGroupName</span></span>
<span data-ttu-id="46461-134">Określa nazwę grupy zasobów, której dotyczy blokada.</span><span class="sxs-lookup"><span data-stu-id="46461-134">Specifies the name of the resource group for which the lock applies.</span></span>
<span data-ttu-id="46461-135">To polecenie cmdlet pobiera blokady dla tej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="46461-135">This cmdlet gets locks for this resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46461-136">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="46461-136">-ResourceName</span></span>
<span data-ttu-id="46461-137">Określa nazwę zasobu, którego dotyczy ten kłódka.</span><span class="sxs-lookup"><span data-stu-id="46461-137">Specifies the name of the resource for which this lock applies.</span></span>
<span data-ttu-id="46461-138">To polecenie cmdlet pobiera blokady dla tego zasobu.</span><span class="sxs-lookup"><span data-stu-id="46461-138">This cmdlet gets locks for this resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46461-139">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="46461-139">-ResourceType</span></span>
<span data-ttu-id="46461-140">Określa typ zasobu, którego dotyczy ten kłódka.</span><span class="sxs-lookup"><span data-stu-id="46461-140">Specifies the resource type of the resource for which this lock applies.</span></span>
<span data-ttu-id="46461-141">To polecenie cmdlet pobiera blokady dla tego zasobu.</span><span class="sxs-lookup"><span data-stu-id="46461-141">This cmdlet gets locks for this resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46461-142">— Zakres</span><span class="sxs-lookup"><span data-stu-id="46461-142">-Scope</span></span>
<span data-ttu-id="46461-143">Określa zakres, do którego ma zastosowanie blokada.</span><span class="sxs-lookup"><span data-stu-id="46461-143">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="46461-144">Polecenie cmdlet pobiera blokady dla tego zakresu.</span><span class="sxs-lookup"><span data-stu-id="46461-144">The cmdlet gets locks for this scope.</span></span>

```yaml
Type: System.String
Parameter Sets: BySpecifiedScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46461-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46461-145">CommonParameters</span></span>
<span data-ttu-id="46461-146">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46461-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46461-147">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="46461-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46461-148">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="46461-148">INPUTS</span></span>

### <span data-ttu-id="46461-149">System.String</span><span class="sxs-lookup"><span data-stu-id="46461-149">System.String</span></span>

## <span data-ttu-id="46461-150">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="46461-150">OUTPUTS</span></span>

### <span data-ttu-id="46461-151">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="46461-151">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="46461-152">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="46461-152">NOTES</span></span>

## <span data-ttu-id="46461-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="46461-153">RELATED LINKS</span></span>

[<span data-ttu-id="46461-154">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="46461-154">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="46461-155">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="46461-155">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)

[<span data-ttu-id="46461-156">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="46461-156">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


