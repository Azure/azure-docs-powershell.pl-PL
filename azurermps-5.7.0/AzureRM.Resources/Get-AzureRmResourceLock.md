---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 3FBF91B8-8EF9-4E05-AD7E-AEFC6EBBFB8E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceLock.md
ms.openlocfilehash: e3d0dfe975a6a76267864b329c3e3130f447cb58
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524962"
---
# <span data-ttu-id="52f28-101">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="52f28-101">Get-AzureRmResourceLock</span></span>

## <span data-ttu-id="52f28-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="52f28-102">SYNOPSIS</span></span>
<span data-ttu-id="52f28-103">Pobiera blokadę zasobu.</span><span class="sxs-lookup"><span data-stu-id="52f28-103">Gets a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52f28-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="52f28-104">SYNTAX</span></span>

### <span data-ttu-id="52f28-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="52f28-105">ByResourceGroup</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="52f28-106">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="52f28-106">ByResourceGroupLevel</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="52f28-107">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="52f28-107">BySpecifiedScope</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="52f28-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="52f28-108">BySubscription</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="52f28-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="52f28-109">BySubscriptionLevel</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="52f28-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="52f28-110">ByTenantLevel</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="52f28-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="52f28-111">ByLockId</span></span>
```
Get-AzureRmResourceLock [-AtScope] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="52f28-112">Opis</span><span class="sxs-lookup"><span data-stu-id="52f28-112">DESCRIPTION</span></span>
<span data-ttu-id="52f28-113">Polecenie cmdlet **Get-AzureRmResourceLock** pobiera blokady zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="52f28-113">The **Get-AzureRmResourceLock** cmdlet gets Azure resource locks.</span></span>

## <span data-ttu-id="52f28-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="52f28-114">EXAMPLES</span></span>

### <span data-ttu-id="52f28-115">Przykład 1: Uzyskaj blokadę</span><span class="sxs-lookup"><span data-stu-id="52f28-115">Example 1: Get a lock</span></span>
```
PS C:\>Get-AzureRmResourceLock -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="52f28-116">To polecenie uzyskuje blokadę zasobu o nazwie ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="52f28-116">This command gets the resource lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="52f28-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="52f28-117">PARAMETERS</span></span>

### <span data-ttu-id="52f28-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="52f28-118">-ApiVersion</span></span>
<span data-ttu-id="52f28-119">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="52f28-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="52f28-120">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="52f28-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52f28-121">-AtScope</span><span class="sxs-lookup"><span data-stu-id="52f28-121">-AtScope</span></span>
<span data-ttu-id="52f28-122">Wskazuje, że to polecenie cmdlet zwraca wszystkie blokady w określonym zakresie lub powyżej określonego zakresu.</span><span class="sxs-lookup"><span data-stu-id="52f28-122">Indicates that this cmdlet returns all locks at or above the specified scope.</span></span>
<span data-ttu-id="52f28-123">Jeśli nie podano tego parametru, polecenie cmdlet zwraca wszystkie blokady w zakresie, powyżej lub poniżej zakresu.</span><span class="sxs-lookup"><span data-stu-id="52f28-123">If you do not specify this parameter, the cmdlet returns all locks at, above, or below the scope.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52f28-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52f28-124">-DefaultProfile</span></span>
<span data-ttu-id="52f28-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="52f28-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52f28-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="52f28-126">-InformationAction</span></span>
<span data-ttu-id="52f28-127">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="52f28-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="52f28-128">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="52f28-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="52f28-129">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="52f28-129">Continue</span></span>
- <span data-ttu-id="52f28-130">Ignorować</span><span class="sxs-lookup"><span data-stu-id="52f28-130">Ignore</span></span>
- <span data-ttu-id="52f28-131">Inquire</span><span class="sxs-lookup"><span data-stu-id="52f28-131">Inquire</span></span>
- <span data-ttu-id="52f28-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="52f28-132">SilentlyContinue</span></span>
- <span data-ttu-id="52f28-133">Przestaw</span><span class="sxs-lookup"><span data-stu-id="52f28-133">Stop</span></span>
- <span data-ttu-id="52f28-134">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="52f28-134">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52f28-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="52f28-135">-InformationVariable</span></span>
<span data-ttu-id="52f28-136">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="52f28-136">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52f28-137">-LockId</span><span class="sxs-lookup"><span data-stu-id="52f28-137">-LockId</span></span>
<span data-ttu-id="52f28-138">Określa identyfikator blokady, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52f28-138">Specifies the ID of the lock that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByLockId
Aliases: Id, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52f28-139">-Kłódkaname</span><span class="sxs-lookup"><span data-stu-id="52f28-139">-LockName</span></span>
<span data-ttu-id="52f28-140">Określa nazwę blokady, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52f28-140">Specifies the name of the lock that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel, BySpecifiedScope, BySubscription, BySubscriptionLevel, ByTenantLevel
Aliases: ExtensionResourceName, Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52f28-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="52f28-141">-Pre</span></span>
<span data-ttu-id="52f28-142">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="52f28-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52f28-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52f28-143">-ResourceGroupName</span></span>
<span data-ttu-id="52f28-144">Określa nazwę grupy zasobów, której dotyczy blokada.</span><span class="sxs-lookup"><span data-stu-id="52f28-144">Specifies the name of the resource group for which the lock applies.</span></span>
<span data-ttu-id="52f28-145">To polecenie cmdlet umożliwia pobieranie blokad dla tej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="52f28-145">This cmdlet gets locks for this resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52f28-146">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="52f28-146">-ResourceName</span></span>
<span data-ttu-id="52f28-147">Określa nazwę zasobu, którego dotyczy ta blokada.</span><span class="sxs-lookup"><span data-stu-id="52f28-147">Specifies the name of the resource for which this lock applies.</span></span>
<span data-ttu-id="52f28-148">To polecenie cmdlet umożliwia blokowanie dla tego zasobu.</span><span class="sxs-lookup"><span data-stu-id="52f28-148">This cmdlet gets locks for this resource.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52f28-149">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="52f28-149">-ResourceType</span></span>
<span data-ttu-id="52f28-150">Określa typ zasobu zasobu, którego dotyczy ta blokada.</span><span class="sxs-lookup"><span data-stu-id="52f28-150">Specifies the resource type of the resource for which this lock applies.</span></span>
<span data-ttu-id="52f28-151">To polecenie cmdlet umożliwia blokowanie dla tego zasobu.</span><span class="sxs-lookup"><span data-stu-id="52f28-151">This cmdlet gets locks for this resource.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52f28-152">-Zakres</span><span class="sxs-lookup"><span data-stu-id="52f28-152">-Scope</span></span>
<span data-ttu-id="52f28-153">Określa zakres, do którego jest stosowana blokada.</span><span class="sxs-lookup"><span data-stu-id="52f28-153">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="52f28-154">Polecenie cmdlet umożliwia blokowanie dla tego zakresu.</span><span class="sxs-lookup"><span data-stu-id="52f28-154">The cmdlet gets locks for this scope.</span></span>

```yaml
Type: String
Parameter Sets: BySpecifiedScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52f28-155">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="52f28-155">-TenantLevel</span></span>
<span data-ttu-id="52f28-156">Wskazuje, że ten aplet polecenia działa na poziomie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="52f28-156">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52f28-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52f28-157">CommonParameters</span></span>
<span data-ttu-id="52f28-158">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52f28-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52f28-159">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52f28-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52f28-160">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="52f28-160">INPUTS</span></span>

### <span data-ttu-id="52f28-161">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="52f28-161">None</span></span>
<span data-ttu-id="52f28-162">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="52f28-162">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="52f28-163">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="52f28-163">OUTPUTS</span></span>

### <span data-ttu-id="52f28-164">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="52f28-164">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="52f28-165">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="52f28-165">NOTES</span></span>

## <span data-ttu-id="52f28-166">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="52f28-166">RELATED LINKS</span></span>

[<span data-ttu-id="52f28-167">Nowe — AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="52f28-167">New-AzureRmResourceLock</span></span>](./New-AzureRmResourceLock.md)

[<span data-ttu-id="52f28-168">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="52f28-168">Remove-AzureRmResourceLock</span></span>](./Remove-AzureRmResourceLock.md)

[<span data-ttu-id="52f28-169">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="52f28-169">Set-AzureRmResourceLock</span></span>](./Set-AzureRmResourceLock.md)


