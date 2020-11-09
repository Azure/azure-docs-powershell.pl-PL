---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 3FBF91B8-8EF9-4E05-AD7E-AEFC6EBBFB8E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceLock.md
ms.openlocfilehash: 2dbbb41ce1ad2ee6fc2279e711722090f4f1a6cc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94308851"
---
# <span data-ttu-id="0edae-101">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="0edae-101">Get-AzResourceLock</span></span>

## <span data-ttu-id="0edae-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0edae-102">SYNOPSIS</span></span>
<span data-ttu-id="0edae-103">Pobiera blokadę zasobu.</span><span class="sxs-lookup"><span data-stu-id="0edae-103">Gets a resource lock.</span></span>

## <span data-ttu-id="0edae-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0edae-104">SYNTAX</span></span>

### <span data-ttu-id="0edae-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0edae-105">ByResourceGroup</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0edae-106">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="0edae-106">ByResourceGroupLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0edae-107">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="0edae-107">BySpecifiedScope</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0edae-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="0edae-108">BySubscription</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0edae-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="0edae-109">BySubscriptionLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0edae-110">ByLockId</span><span class="sxs-lookup"><span data-stu-id="0edae-110">ByLockId</span></span>
```
Get-AzResourceLock [-AtScope] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0edae-111">Opis</span><span class="sxs-lookup"><span data-stu-id="0edae-111">DESCRIPTION</span></span>
<span data-ttu-id="0edae-112">Polecenie cmdlet **Get-AzResourceLock** pobiera blokady zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0edae-112">The **Get-AzResourceLock** cmdlet gets Azure resource locks.</span></span>

## <span data-ttu-id="0edae-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0edae-113">EXAMPLES</span></span>

### <span data-ttu-id="0edae-114">Przykład 1: Uzyskaj blokadę</span><span class="sxs-lookup"><span data-stu-id="0edae-114">Example 1: Get a lock</span></span>
```
PS C:\>Get-AzResourceLock -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="0edae-115">To polecenie uzyskuje blokadę zasobu o nazwie ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="0edae-115">This command gets the resource lock named ContosoSiteLock.</span></span>

### <span data-ttu-id="0edae-116">Przykład 2: Uzyskaj blokady na poziomie grup zasobów lub większe</span><span class="sxs-lookup"><span data-stu-id="0edae-116">Example 2: Get locks at resource group level or higher</span></span>
```
PS C:\> Get-AzResourceLock -ResourceGroupName "ResourceGroup11" -AtScope
```

<span data-ttu-id="0edae-117">To polecenie umożliwia pobieranie blokad zasobów z grupy zasobów lub subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="0edae-117">This command gets the resource locks on the resource group or the subscription.</span></span>

## <span data-ttu-id="0edae-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0edae-118">PARAMETERS</span></span>

### <span data-ttu-id="0edae-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="0edae-119">-ApiVersion</span></span>
<span data-ttu-id="0edae-120">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="0edae-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="0edae-121">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="0edae-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="0edae-122">-AtScope</span><span class="sxs-lookup"><span data-stu-id="0edae-122">-AtScope</span></span>
<span data-ttu-id="0edae-123">Wskazuje, że to polecenie cmdlet zwraca wszystkie blokady w określonym zakresie lub powyżej określonego zakresu.</span><span class="sxs-lookup"><span data-stu-id="0edae-123">Indicates that this cmdlet returns all locks at or above the specified scope.</span></span>
<span data-ttu-id="0edae-124">Jeśli nie podano tego parametru, polecenie cmdlet zwraca wszystkie blokady w zakresie, powyżej lub poniżej zakresu.</span><span class="sxs-lookup"><span data-stu-id="0edae-124">If you do not specify this parameter, the cmdlet returns all locks at, above, or below the scope.</span></span>

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

### <span data-ttu-id="0edae-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0edae-125">-DefaultProfile</span></span>
<span data-ttu-id="0edae-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="0edae-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0edae-127">-LockId</span><span class="sxs-lookup"><span data-stu-id="0edae-127">-LockId</span></span>
<span data-ttu-id="0edae-128">Określa identyfikator blokady, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0edae-128">Specifies the ID of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="0edae-129">-Kłódkaname</span><span class="sxs-lookup"><span data-stu-id="0edae-129">-LockName</span></span>
<span data-ttu-id="0edae-130">Określa nazwę blokady, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0edae-130">Specifies the name of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="0edae-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="0edae-131">-Pre</span></span>
<span data-ttu-id="0edae-132">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="0edae-132">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="0edae-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0edae-133">-ResourceGroupName</span></span>
<span data-ttu-id="0edae-134">Określa nazwę grupy zasobów, której dotyczy blokada.</span><span class="sxs-lookup"><span data-stu-id="0edae-134">Specifies the name of the resource group for which the lock applies.</span></span>
<span data-ttu-id="0edae-135">To polecenie cmdlet umożliwia pobieranie blokad dla tej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0edae-135">This cmdlet gets locks for this resource group.</span></span>

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

### <span data-ttu-id="0edae-136">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="0edae-136">-ResourceName</span></span>
<span data-ttu-id="0edae-137">Określa nazwę zasobu, którego dotyczy ta blokada.</span><span class="sxs-lookup"><span data-stu-id="0edae-137">Specifies the name of the resource for which this lock applies.</span></span>
<span data-ttu-id="0edae-138">To polecenie cmdlet umożliwia blokowanie dla tego zasobu.</span><span class="sxs-lookup"><span data-stu-id="0edae-138">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="0edae-139">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="0edae-139">-ResourceType</span></span>
<span data-ttu-id="0edae-140">Określa typ zasobu zasobu, którego dotyczy ta blokada.</span><span class="sxs-lookup"><span data-stu-id="0edae-140">Specifies the resource type of the resource for which this lock applies.</span></span>
<span data-ttu-id="0edae-141">To polecenie cmdlet umożliwia blokowanie dla tego zasobu.</span><span class="sxs-lookup"><span data-stu-id="0edae-141">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="0edae-142">-Zakres</span><span class="sxs-lookup"><span data-stu-id="0edae-142">-Scope</span></span>
<span data-ttu-id="0edae-143">Określa zakres, do którego jest stosowana blokada.</span><span class="sxs-lookup"><span data-stu-id="0edae-143">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="0edae-144">Polecenie cmdlet umożliwia blokowanie dla tego zakresu.</span><span class="sxs-lookup"><span data-stu-id="0edae-144">The cmdlet gets locks for this scope.</span></span>

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

### <span data-ttu-id="0edae-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0edae-145">CommonParameters</span></span>
<span data-ttu-id="0edae-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0edae-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0edae-147">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0edae-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0edae-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0edae-148">INPUTS</span></span>

### <span data-ttu-id="0edae-149">System. String</span><span class="sxs-lookup"><span data-stu-id="0edae-149">System.String</span></span>

## <span data-ttu-id="0edae-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0edae-150">OUTPUTS</span></span>

### <span data-ttu-id="0edae-151">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="0edae-151">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="0edae-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0edae-152">NOTES</span></span>

## <span data-ttu-id="0edae-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0edae-153">RELATED LINKS</span></span>

[<span data-ttu-id="0edae-154">Nowe — AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="0edae-154">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="0edae-155">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="0edae-155">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)

[<span data-ttu-id="0edae-156">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="0edae-156">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


