---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 3FBF91B8-8EF9-4E05-AD7E-AEFC6EBBFB8E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresourcelock
schema: 2.0.0
ms.openlocfilehash: 81e7ab170dc43af0cf712fd9be3e831f33f7fd97
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898642"
---
# <span data-ttu-id="bd663-101">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="bd663-101">Get-AzureRmResourceLock</span></span>

## <span data-ttu-id="bd663-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bd663-102">SYNOPSIS</span></span>
<span data-ttu-id="bd663-103">Pobiera blokadę zasobu.</span><span class="sxs-lookup"><span data-stu-id="bd663-103">Gets a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd663-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bd663-104">SYNTAX</span></span>

### <span data-ttu-id="bd663-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="bd663-105">ByResourceGroup</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="bd663-106">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="bd663-106">ByResourceGroupLevel</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="bd663-107">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="bd663-107">BySpecifiedScope</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="bd663-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="bd663-108">BySubscription</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="bd663-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="bd663-109">BySubscriptionLevel</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="bd663-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="bd663-110">ByTenantLevel</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="bd663-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="bd663-111">ByLockId</span></span>
```
Get-AzureRmResourceLock [-AtScope] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="bd663-112">Opis</span><span class="sxs-lookup"><span data-stu-id="bd663-112">DESCRIPTION</span></span>
<span data-ttu-id="bd663-113">Polecenie cmdlet **Get-AzureRmResourceLock** pobiera blokady zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="bd663-113">The **Get-AzureRmResourceLock** cmdlet gets Azure resource locks.</span></span>

## <span data-ttu-id="bd663-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bd663-114">EXAMPLES</span></span>

### <span data-ttu-id="bd663-115">Przykład 1: Uzyskaj blokadę</span><span class="sxs-lookup"><span data-stu-id="bd663-115">Example 1: Get a lock</span></span>
```
PS C:\>Get-AzureRmResourceLock -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="bd663-116">To polecenie uzyskuje blokadę zasobu o nazwie ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="bd663-116">This command gets the resource lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="bd663-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bd663-117">PARAMETERS</span></span>

### <span data-ttu-id="bd663-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="bd663-118">-ApiVersion</span></span>
<span data-ttu-id="bd663-119">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="bd663-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="bd663-120">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="bd663-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="bd663-121">-AtScope</span><span class="sxs-lookup"><span data-stu-id="bd663-121">-AtScope</span></span>
<span data-ttu-id="bd663-122">Wskazuje, że to polecenie cmdlet zwraca wszystkie blokady w określonym zakresie lub powyżej określonego zakresu.</span><span class="sxs-lookup"><span data-stu-id="bd663-122">Indicates that this cmdlet returns all locks at or above the specified scope.</span></span>
<span data-ttu-id="bd663-123">Jeśli nie podano tego parametru, polecenie cmdlet zwraca wszystkie blokady w zakresie, powyżej lub poniżej zakresu.</span><span class="sxs-lookup"><span data-stu-id="bd663-123">If you do not specify this parameter, the cmdlet returns all locks at, above, or below the scope.</span></span>

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

### <span data-ttu-id="bd663-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd663-124">-DefaultProfile</span></span>
<span data-ttu-id="bd663-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="bd663-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bd663-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="bd663-126">-InformationAction</span></span>
<span data-ttu-id="bd663-127">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="bd663-127">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="bd663-128">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="bd663-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bd663-129">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="bd663-129">Continue</span></span>
- <span data-ttu-id="bd663-130">Ignorować</span><span class="sxs-lookup"><span data-stu-id="bd663-130">Ignore</span></span>
- <span data-ttu-id="bd663-131">Inquire</span><span class="sxs-lookup"><span data-stu-id="bd663-131">Inquire</span></span>
- <span data-ttu-id="bd663-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="bd663-132">SilentlyContinue</span></span>
- <span data-ttu-id="bd663-133">Przestaw</span><span class="sxs-lookup"><span data-stu-id="bd663-133">Stop</span></span>
- <span data-ttu-id="bd663-134">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="bd663-134">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd663-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="bd663-135">-InformationVariable</span></span>
<span data-ttu-id="bd663-136">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="bd663-136">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd663-137">-LockId</span><span class="sxs-lookup"><span data-stu-id="bd663-137">-LockId</span></span>
<span data-ttu-id="bd663-138">Określa identyfikator blokady, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd663-138">Specifies the ID of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="bd663-139">-Kłódkaname</span><span class="sxs-lookup"><span data-stu-id="bd663-139">-LockName</span></span>
<span data-ttu-id="bd663-140">Określa nazwę blokady, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd663-140">Specifies the name of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="bd663-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="bd663-141">-Pre</span></span>
<span data-ttu-id="bd663-142">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="bd663-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="bd663-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd663-143">-ResourceGroupName</span></span>
<span data-ttu-id="bd663-144">Określa nazwę grupy zasobów, której dotyczy blokada.</span><span class="sxs-lookup"><span data-stu-id="bd663-144">Specifies the name of the resource group for which the lock applies.</span></span>
<span data-ttu-id="bd663-145">To polecenie cmdlet umożliwia pobieranie blokad dla tej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="bd663-145">This cmdlet gets locks for this resource group.</span></span>

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

### <span data-ttu-id="bd663-146">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="bd663-146">-ResourceName</span></span>
<span data-ttu-id="bd663-147">Określa nazwę zasobu, którego dotyczy ta blokada.</span><span class="sxs-lookup"><span data-stu-id="bd663-147">Specifies the name of the resource for which this lock applies.</span></span>
<span data-ttu-id="bd663-148">To polecenie cmdlet umożliwia blokowanie dla tego zasobu.</span><span class="sxs-lookup"><span data-stu-id="bd663-148">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="bd663-149">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="bd663-149">-ResourceType</span></span>
<span data-ttu-id="bd663-150">Określa typ zasobu zasobu, którego dotyczy ta blokada.</span><span class="sxs-lookup"><span data-stu-id="bd663-150">Specifies the resource type of the resource for which this lock applies.</span></span>
<span data-ttu-id="bd663-151">To polecenie cmdlet umożliwia blokowanie dla tego zasobu.</span><span class="sxs-lookup"><span data-stu-id="bd663-151">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="bd663-152">-Zakres</span><span class="sxs-lookup"><span data-stu-id="bd663-152">-Scope</span></span>
<span data-ttu-id="bd663-153">Określa zakres, do którego jest stosowana blokada.</span><span class="sxs-lookup"><span data-stu-id="bd663-153">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="bd663-154">Polecenie cmdlet umożliwia blokowanie dla tego zakresu.</span><span class="sxs-lookup"><span data-stu-id="bd663-154">The cmdlet gets locks for this scope.</span></span>

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

### <span data-ttu-id="bd663-155">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="bd663-155">-TenantLevel</span></span>
<span data-ttu-id="bd663-156">Wskazuje, że ten aplet polecenia działa na poziomie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="bd663-156">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="bd663-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd663-157">CommonParameters</span></span>
<span data-ttu-id="bd663-158">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd663-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd663-159">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd663-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd663-160">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bd663-160">INPUTS</span></span>

## <span data-ttu-id="bd663-161">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bd663-161">OUTPUTS</span></span>

## <span data-ttu-id="bd663-162">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bd663-162">NOTES</span></span>

## <span data-ttu-id="bd663-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bd663-163">RELATED LINKS</span></span>

[<span data-ttu-id="bd663-164">Nowe — AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="bd663-164">New-AzureRmResourceLock</span></span>](./New-AzureRmResourceLock.md)

[<span data-ttu-id="bd663-165">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="bd663-165">Remove-AzureRmResourceLock</span></span>](./Remove-AzureRmResourceLock.md)

[<span data-ttu-id="bd663-166">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="bd663-166">Set-AzureRmResourceLock</span></span>](./Set-AzureRmResourceLock.md)


