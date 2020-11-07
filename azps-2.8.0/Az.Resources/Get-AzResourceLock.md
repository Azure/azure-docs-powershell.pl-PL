---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 3FBF91B8-8EF9-4E05-AD7E-AEFC6EBBFB8E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceLock.md
ms.openlocfilehash: 7c9a9da46da232e6b8a7e81e9b698d2b76513c71
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873387"
---
# <span data-ttu-id="ee21b-101">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="ee21b-101">Get-AzResourceLock</span></span>

## <span data-ttu-id="ee21b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ee21b-102">SYNOPSIS</span></span>
<span data-ttu-id="ee21b-103">Pobiera blokadę zasobu.</span><span class="sxs-lookup"><span data-stu-id="ee21b-103">Gets a resource lock.</span></span>

## <span data-ttu-id="ee21b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ee21b-104">SYNTAX</span></span>

### <span data-ttu-id="ee21b-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ee21b-105">ByResourceGroup</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ee21b-106">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="ee21b-106">ByResourceGroupLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ee21b-107">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="ee21b-107">BySpecifiedScope</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ee21b-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="ee21b-108">BySubscription</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ee21b-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="ee21b-109">BySubscriptionLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ee21b-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="ee21b-110">ByTenantLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String> [-TenantLevel]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ee21b-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="ee21b-111">ByLockId</span></span>
```
Get-AzResourceLock [-AtScope] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ee21b-112">Opis</span><span class="sxs-lookup"><span data-stu-id="ee21b-112">DESCRIPTION</span></span>
<span data-ttu-id="ee21b-113">Polecenie cmdlet **Get-AzResourceLock** pobiera blokady zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ee21b-113">The **Get-AzResourceLock** cmdlet gets Azure resource locks.</span></span>

## <span data-ttu-id="ee21b-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ee21b-114">EXAMPLES</span></span>

### <span data-ttu-id="ee21b-115">Przykład 1: Uzyskaj blokadę</span><span class="sxs-lookup"><span data-stu-id="ee21b-115">Example 1: Get a lock</span></span>
```
PS C:\>Get-AzResourceLock -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="ee21b-116">To polecenie uzyskuje blokadę zasobu o nazwie ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="ee21b-116">This command gets the resource lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="ee21b-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ee21b-117">PARAMETERS</span></span>

### <span data-ttu-id="ee21b-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="ee21b-118">-ApiVersion</span></span>
<span data-ttu-id="ee21b-119">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="ee21b-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="ee21b-120">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="ee21b-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="ee21b-121">-AtScope</span><span class="sxs-lookup"><span data-stu-id="ee21b-121">-AtScope</span></span>
<span data-ttu-id="ee21b-122">Wskazuje, że to polecenie cmdlet zwraca wszystkie blokady w określonym zakresie lub powyżej określonego zakresu.</span><span class="sxs-lookup"><span data-stu-id="ee21b-122">Indicates that this cmdlet returns all locks at or above the specified scope.</span></span>
<span data-ttu-id="ee21b-123">Jeśli nie podano tego parametru, polecenie cmdlet zwraca wszystkie blokady w zakresie, powyżej lub poniżej zakresu.</span><span class="sxs-lookup"><span data-stu-id="ee21b-123">If you do not specify this parameter, the cmdlet returns all locks at, above, or below the scope.</span></span>

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

### <span data-ttu-id="ee21b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee21b-124">-DefaultProfile</span></span>
<span data-ttu-id="ee21b-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="ee21b-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ee21b-126">-LockId</span><span class="sxs-lookup"><span data-stu-id="ee21b-126">-LockId</span></span>
<span data-ttu-id="ee21b-127">Określa identyfikator blokady, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee21b-127">Specifies the ID of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="ee21b-128">-Kłódkaname</span><span class="sxs-lookup"><span data-stu-id="ee21b-128">-LockName</span></span>
<span data-ttu-id="ee21b-129">Określa nazwę blokady, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee21b-129">Specifies the name of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="ee21b-130">-Pre</span><span class="sxs-lookup"><span data-stu-id="ee21b-130">-Pre</span></span>
<span data-ttu-id="ee21b-131">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="ee21b-131">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="ee21b-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee21b-132">-ResourceGroupName</span></span>
<span data-ttu-id="ee21b-133">Określa nazwę grupy zasobów, której dotyczy blokada.</span><span class="sxs-lookup"><span data-stu-id="ee21b-133">Specifies the name of the resource group for which the lock applies.</span></span>
<span data-ttu-id="ee21b-134">To polecenie cmdlet umożliwia pobieranie blokad dla tej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ee21b-134">This cmdlet gets locks for this resource group.</span></span>

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

### <span data-ttu-id="ee21b-135">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="ee21b-135">-ResourceName</span></span>
<span data-ttu-id="ee21b-136">Określa nazwę zasobu, którego dotyczy ta blokada.</span><span class="sxs-lookup"><span data-stu-id="ee21b-136">Specifies the name of the resource for which this lock applies.</span></span>
<span data-ttu-id="ee21b-137">To polecenie cmdlet umożliwia blokowanie dla tego zasobu.</span><span class="sxs-lookup"><span data-stu-id="ee21b-137">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="ee21b-138">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="ee21b-138">-ResourceType</span></span>
<span data-ttu-id="ee21b-139">Określa typ zasobu zasobu, którego dotyczy ta blokada.</span><span class="sxs-lookup"><span data-stu-id="ee21b-139">Specifies the resource type of the resource for which this lock applies.</span></span>
<span data-ttu-id="ee21b-140">To polecenie cmdlet umożliwia blokowanie dla tego zasobu.</span><span class="sxs-lookup"><span data-stu-id="ee21b-140">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="ee21b-141">-Zakres</span><span class="sxs-lookup"><span data-stu-id="ee21b-141">-Scope</span></span>
<span data-ttu-id="ee21b-142">Określa zakres, do którego jest stosowana blokada.</span><span class="sxs-lookup"><span data-stu-id="ee21b-142">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="ee21b-143">Polecenie cmdlet umożliwia blokowanie dla tego zakresu.</span><span class="sxs-lookup"><span data-stu-id="ee21b-143">The cmdlet gets locks for this scope.</span></span>

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

### <span data-ttu-id="ee21b-144">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="ee21b-144">-TenantLevel</span></span>
<span data-ttu-id="ee21b-145">Wskazuje, że ten aplet polecenia działa na poziomie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="ee21b-145">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="ee21b-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee21b-146">CommonParameters</span></span>
<span data-ttu-id="ee21b-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee21b-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee21b-148">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee21b-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee21b-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ee21b-149">INPUTS</span></span>

### <span data-ttu-id="ee21b-150">System. String</span><span class="sxs-lookup"><span data-stu-id="ee21b-150">System.String</span></span>

## <span data-ttu-id="ee21b-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ee21b-151">OUTPUTS</span></span>

### <span data-ttu-id="ee21b-152">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="ee21b-152">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="ee21b-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ee21b-153">NOTES</span></span>

## <span data-ttu-id="ee21b-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ee21b-154">RELATED LINKS</span></span>

[<span data-ttu-id="ee21b-155">Nowe — AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="ee21b-155">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="ee21b-156">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="ee21b-156">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)

[<span data-ttu-id="ee21b-157">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="ee21b-157">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


