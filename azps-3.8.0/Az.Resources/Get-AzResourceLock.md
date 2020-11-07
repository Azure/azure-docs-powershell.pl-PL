---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 3FBF91B8-8EF9-4E05-AD7E-AEFC6EBBFB8E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceLock.md
ms.openlocfilehash: ea0ee8e46c70e6dd61e352ce0e7bd5da391c0c66
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93895330"
---
# <span data-ttu-id="254aa-101">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="254aa-101">Get-AzResourceLock</span></span>

## <span data-ttu-id="254aa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="254aa-102">SYNOPSIS</span></span>
<span data-ttu-id="254aa-103">Pobiera blokadę zasobu.</span><span class="sxs-lookup"><span data-stu-id="254aa-103">Gets a resource lock.</span></span>

## <span data-ttu-id="254aa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="254aa-104">SYNTAX</span></span>

### <span data-ttu-id="254aa-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="254aa-105">ByResourceGroup</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="254aa-106">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="254aa-106">ByResourceGroupLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="254aa-107">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="254aa-107">BySpecifiedScope</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="254aa-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="254aa-108">BySubscription</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="254aa-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="254aa-109">BySubscriptionLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="254aa-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="254aa-110">ByTenantLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String> [-TenantLevel]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="254aa-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="254aa-111">ByLockId</span></span>
```
Get-AzResourceLock [-AtScope] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="254aa-112">Opis</span><span class="sxs-lookup"><span data-stu-id="254aa-112">DESCRIPTION</span></span>
<span data-ttu-id="254aa-113">Polecenie cmdlet **Get-AzResourceLock** pobiera blokady zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="254aa-113">The **Get-AzResourceLock** cmdlet gets Azure resource locks.</span></span>

## <span data-ttu-id="254aa-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="254aa-114">EXAMPLES</span></span>

### <span data-ttu-id="254aa-115">Przykład 1: Uzyskaj blokadę</span><span class="sxs-lookup"><span data-stu-id="254aa-115">Example 1: Get a lock</span></span>
```
PS C:\>Get-AzResourceLock -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="254aa-116">To polecenie uzyskuje blokadę zasobu o nazwie ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="254aa-116">This command gets the resource lock named ContosoSiteLock.</span></span>

### <span data-ttu-id="254aa-117">Przykład 2: Uzyskaj blokady na poziomie grup zasobów lub większe</span><span class="sxs-lookup"><span data-stu-id="254aa-117">Example 2: Get locks at resource group level or higher</span></span>
```
PS C:\> Get-AzResourceLock -ResourceGroupName "ResourceGroup11" -AtScope
```

<span data-ttu-id="254aa-118">To polecenie umożliwia pobieranie blokad zasobów z grupy zasobów lub subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="254aa-118">This command gets the resource locks on the resource group or the subscription.</span></span>

## <span data-ttu-id="254aa-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="254aa-119">PARAMETERS</span></span>

### <span data-ttu-id="254aa-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="254aa-120">-ApiVersion</span></span>
<span data-ttu-id="254aa-121">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="254aa-121">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="254aa-122">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="254aa-122">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="254aa-123">-AtScope</span><span class="sxs-lookup"><span data-stu-id="254aa-123">-AtScope</span></span>
<span data-ttu-id="254aa-124">Wskazuje, że to polecenie cmdlet zwraca wszystkie blokady w określonym zakresie lub powyżej określonego zakresu.</span><span class="sxs-lookup"><span data-stu-id="254aa-124">Indicates that this cmdlet returns all locks at or above the specified scope.</span></span>
<span data-ttu-id="254aa-125">Jeśli nie podano tego parametru, polecenie cmdlet zwraca wszystkie blokady w zakresie, powyżej lub poniżej zakresu.</span><span class="sxs-lookup"><span data-stu-id="254aa-125">If you do not specify this parameter, the cmdlet returns all locks at, above, or below the scope.</span></span>

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

### <span data-ttu-id="254aa-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="254aa-126">-DefaultProfile</span></span>
<span data-ttu-id="254aa-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="254aa-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="254aa-128">-LockId</span><span class="sxs-lookup"><span data-stu-id="254aa-128">-LockId</span></span>
<span data-ttu-id="254aa-129">Określa identyfikator blokady, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="254aa-129">Specifies the ID of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="254aa-130">-Kłódkaname</span><span class="sxs-lookup"><span data-stu-id="254aa-130">-LockName</span></span>
<span data-ttu-id="254aa-131">Określa nazwę blokady, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="254aa-131">Specifies the name of the lock that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel, BySpecifiedScope, BySubscription, BySubscriptionLevel, ByTenantLevel
Aliases: ExtensionResourceName, Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="254aa-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="254aa-132">-Pre</span></span>
<span data-ttu-id="254aa-133">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="254aa-133">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="254aa-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="254aa-134">-ResourceGroupName</span></span>
<span data-ttu-id="254aa-135">Określa nazwę grupy zasobów, której dotyczy blokada.</span><span class="sxs-lookup"><span data-stu-id="254aa-135">Specifies the name of the resource group for which the lock applies.</span></span>
<span data-ttu-id="254aa-136">To polecenie cmdlet umożliwia pobieranie blokad dla tej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="254aa-136">This cmdlet gets locks for this resource group.</span></span>

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

### <span data-ttu-id="254aa-137">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="254aa-137">-ResourceName</span></span>
<span data-ttu-id="254aa-138">Określa nazwę zasobu, którego dotyczy ta blokada.</span><span class="sxs-lookup"><span data-stu-id="254aa-138">Specifies the name of the resource for which this lock applies.</span></span>
<span data-ttu-id="254aa-139">To polecenie cmdlet umożliwia blokowanie dla tego zasobu.</span><span class="sxs-lookup"><span data-stu-id="254aa-139">This cmdlet gets locks for this resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="254aa-140">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="254aa-140">-ResourceType</span></span>
<span data-ttu-id="254aa-141">Określa typ zasobu zasobu, którego dotyczy ta blokada.</span><span class="sxs-lookup"><span data-stu-id="254aa-141">Specifies the resource type of the resource for which this lock applies.</span></span>
<span data-ttu-id="254aa-142">To polecenie cmdlet umożliwia blokowanie dla tego zasobu.</span><span class="sxs-lookup"><span data-stu-id="254aa-142">This cmdlet gets locks for this resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="254aa-143">-Zakres</span><span class="sxs-lookup"><span data-stu-id="254aa-143">-Scope</span></span>
<span data-ttu-id="254aa-144">Określa zakres, do którego jest stosowana blokada.</span><span class="sxs-lookup"><span data-stu-id="254aa-144">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="254aa-145">Polecenie cmdlet umożliwia blokowanie dla tego zakresu.</span><span class="sxs-lookup"><span data-stu-id="254aa-145">The cmdlet gets locks for this scope.</span></span>

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

### <span data-ttu-id="254aa-146">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="254aa-146">-TenantLevel</span></span>
<span data-ttu-id="254aa-147">Wskazuje, że ten aplet polecenia działa na poziomie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="254aa-147">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="254aa-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="254aa-148">CommonParameters</span></span>
<span data-ttu-id="254aa-149">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="254aa-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="254aa-150">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="254aa-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="254aa-151">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="254aa-151">INPUTS</span></span>

### <span data-ttu-id="254aa-152">System. String</span><span class="sxs-lookup"><span data-stu-id="254aa-152">System.String</span></span>

## <span data-ttu-id="254aa-153">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="254aa-153">OUTPUTS</span></span>

### <span data-ttu-id="254aa-154">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="254aa-154">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="254aa-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="254aa-155">NOTES</span></span>

## <span data-ttu-id="254aa-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="254aa-156">RELATED LINKS</span></span>

[<span data-ttu-id="254aa-157">Nowe — AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="254aa-157">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="254aa-158">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="254aa-158">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)

[<span data-ttu-id="254aa-159">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="254aa-159">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


