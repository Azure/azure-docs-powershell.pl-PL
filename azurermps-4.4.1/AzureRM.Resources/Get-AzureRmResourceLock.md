---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 3FBF91B8-8EF9-4E05-AD7E-AEFC6EBBFB8E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceLock.md
ms.openlocfilehash: 51fc1b96734d269fda3e09d3a22122b18fe3943a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549904"
---
# <span data-ttu-id="9d3b4-101">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="9d3b4-101">Get-AzureRmResourceLock</span></span>

## <span data-ttu-id="9d3b4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9d3b4-102">SYNOPSIS</span></span>
<span data-ttu-id="9d3b4-103">Pobiera blokadę zasobu.</span><span class="sxs-lookup"><span data-stu-id="9d3b4-103">Gets a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d3b4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9d3b4-104">SYNTAX</span></span>

### <span data-ttu-id="9d3b4-105">Blokada zakresu grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9d3b4-105">A lock at the resource group scope.</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="9d3b4-106">Blokada zakresu zasobów grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9d3b4-106">A lock at the resource group resource scope.</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="9d3b4-107">Blokada w określonym zakresie.</span><span class="sxs-lookup"><span data-stu-id="9d3b4-107">A lock at the specified scope.</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="9d3b4-108">Blokada zakresu subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="9d3b4-108">A lock at the subscription scope.</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="9d3b4-109">Blokada w zakresie zasobów subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="9d3b4-109">A lock at the subscription resource scope.</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="9d3b4-110">Blokada w zakresie zasobów dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="9d3b4-110">A lock at the tenant resource scope.</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="9d3b4-111">Blokada za pomocą identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="9d3b4-111">A lock, by Id.</span></span>
```
Get-AzureRmResourceLock [-AtScope] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="9d3b4-112">Opis</span><span class="sxs-lookup"><span data-stu-id="9d3b4-112">DESCRIPTION</span></span>
<span data-ttu-id="9d3b4-113">Polecenie cmdlet **Get-AzureRmResourceLock** pobiera blokady zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9d3b4-113">The **Get-AzureRmResourceLock** cmdlet gets Azure resource locks.</span></span>

## <span data-ttu-id="9d3b4-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9d3b4-114">EXAMPLES</span></span>

### <span data-ttu-id="9d3b4-115">Przykład 1: Uzyskaj blokadę</span><span class="sxs-lookup"><span data-stu-id="9d3b4-115">Example 1: Get a lock</span></span>
```
PS C:\>Get-AzureRmResourceLock -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="9d3b4-116">To polecenie uzyskuje blokadę zasobu o nazwie ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="9d3b4-116">This command gets the resource lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="9d3b4-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9d3b4-117">PARAMETERS</span></span>

### <span data-ttu-id="9d3b4-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="9d3b4-118">-ApiVersion</span></span>
<span data-ttu-id="9d3b4-119">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="9d3b4-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="9d3b4-120">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="9d3b4-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="9d3b4-121">-AtScope</span><span class="sxs-lookup"><span data-stu-id="9d3b4-121">-AtScope</span></span>
<span data-ttu-id="9d3b4-122">Wskazuje, że to polecenie cmdlet zwraca wszystkie blokady w określonym zakresie lub powyżej określonego zakresu.</span><span class="sxs-lookup"><span data-stu-id="9d3b4-122">Indicates that this cmdlet returns all locks at or above the specified scope.</span></span>
<span data-ttu-id="9d3b4-123">Jeśli nie podano tego parametru, polecenie cmdlet zwraca wszystkie blokady w zakresie, powyżej lub poniżej zakresu.</span><span class="sxs-lookup"><span data-stu-id="9d3b4-123">If you do not specify this parameter, the cmdlet returns all locks at, above, or below the scope.</span></span>

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

### <span data-ttu-id="9d3b4-124">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="9d3b4-124">-InformationAction</span></span>
<span data-ttu-id="9d3b4-125">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="9d3b4-125">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="9d3b4-126">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="9d3b4-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9d3b4-127">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="9d3b4-127">Continue</span></span>
- <span data-ttu-id="9d3b4-128">Ignorować</span><span class="sxs-lookup"><span data-stu-id="9d3b4-128">Ignore</span></span>
- <span data-ttu-id="9d3b4-129">Inquire</span><span class="sxs-lookup"><span data-stu-id="9d3b4-129">Inquire</span></span>
- <span data-ttu-id="9d3b4-130">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="9d3b4-130">SilentlyContinue</span></span>
- <span data-ttu-id="9d3b4-131">Przestaw</span><span class="sxs-lookup"><span data-stu-id="9d3b4-131">Stop</span></span>
- <span data-ttu-id="9d3b4-132">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="9d3b4-132">Suspend</span></span>

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

### <span data-ttu-id="9d3b4-133">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="9d3b4-133">-InformationVariable</span></span>
<span data-ttu-id="9d3b4-134">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="9d3b4-134">Specifies an information variable.</span></span>

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

### <span data-ttu-id="9d3b4-135">-LockId</span><span class="sxs-lookup"><span data-stu-id="9d3b4-135">-LockId</span></span>
<span data-ttu-id="9d3b4-136">Określa identyfikator blokady, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d3b4-136">Specifies the ID of the lock that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock, by Id.
Aliases: Id, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d3b4-137">-Kłódkaname</span><span class="sxs-lookup"><span data-stu-id="9d3b4-137">-LockName</span></span>
<span data-ttu-id="9d3b4-138">Określa nazwę blokady, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d3b4-138">Specifies the name of the lock that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the resource group scope., A lock at the resource group resource scope., A lock at the specified scope., A lock at the subscription scope., A lock at the subscription resource scope., A lock at the tenant resource scope.
Aliases: ExtensionResourceName, Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d3b4-139">-Pre</span><span class="sxs-lookup"><span data-stu-id="9d3b4-139">-Pre</span></span>
<span data-ttu-id="9d3b4-140">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="9d3b4-140">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="9d3b4-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d3b4-141">-ResourceGroupName</span></span>
<span data-ttu-id="9d3b4-142">Określa nazwę grupy zasobów, której dotyczy blokada.</span><span class="sxs-lookup"><span data-stu-id="9d3b4-142">Specifies the name of the resource group for which the lock applies.</span></span>
<span data-ttu-id="9d3b4-143">To polecenie cmdlet umożliwia pobieranie blokad dla tej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9d3b4-143">This cmdlet gets locks for this resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the resource group scope., A lock at the resource group resource scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d3b4-144">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="9d3b4-144">-ResourceName</span></span>
<span data-ttu-id="9d3b4-145">Określa nazwę zasobu, którego dotyczy ta blokada.</span><span class="sxs-lookup"><span data-stu-id="9d3b4-145">Specifies the name of the resource for which this lock applies.</span></span>
<span data-ttu-id="9d3b4-146">To polecenie cmdlet umożliwia blokowanie dla tego zasobu.</span><span class="sxs-lookup"><span data-stu-id="9d3b4-146">This cmdlet gets locks for this resource.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the resource group resource scope., A lock at the subscription resource scope., A lock at the tenant resource scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d3b4-147">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="9d3b4-147">-ResourceType</span></span>
<span data-ttu-id="9d3b4-148">Określa typ zasobu zasobu, którego dotyczy ta blokada.</span><span class="sxs-lookup"><span data-stu-id="9d3b4-148">Specifies the resource type of the resource for which this lock applies.</span></span>
<span data-ttu-id="9d3b4-149">To polecenie cmdlet umożliwia blokowanie dla tego zasobu.</span><span class="sxs-lookup"><span data-stu-id="9d3b4-149">This cmdlet gets locks for this resource.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the resource group resource scope., A lock at the subscription resource scope., A lock at the tenant resource scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d3b4-150">-Zakres</span><span class="sxs-lookup"><span data-stu-id="9d3b4-150">-Scope</span></span>
<span data-ttu-id="9d3b4-151">Określa zakres, do którego jest stosowana blokada.</span><span class="sxs-lookup"><span data-stu-id="9d3b4-151">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="9d3b4-152">Polecenie cmdlet umożliwia blokowanie dla tego zakresu.</span><span class="sxs-lookup"><span data-stu-id="9d3b4-152">The cmdlet gets locks for this scope.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the specified scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d3b4-153">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="9d3b4-153">-TenantLevel</span></span>
<span data-ttu-id="9d3b4-154">Wskazuje, że ten aplet polecenia działa na poziomie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="9d3b4-154">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: A lock at the tenant resource scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d3b4-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d3b4-155">-DefaultProfile</span></span>
<span data-ttu-id="9d3b4-156">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9d3b4-156">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d3b4-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d3b4-157">CommonParameters</span></span>
<span data-ttu-id="9d3b4-158">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d3b4-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d3b4-159">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d3b4-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d3b4-160">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9d3b4-160">INPUTS</span></span>

## <span data-ttu-id="9d3b4-161">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9d3b4-161">OUTPUTS</span></span>

### <span data-ttu-id="9d3b4-162">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="9d3b4-162">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="9d3b4-163">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9d3b4-163">NOTES</span></span>

## <span data-ttu-id="9d3b4-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9d3b4-164">RELATED LINKS</span></span>

[<span data-ttu-id="9d3b4-165">Nowe — AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="9d3b4-165">New-AzureRmResourceLock</span></span>](./New-AzureRmResourceLock.md)

[<span data-ttu-id="9d3b4-166">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="9d3b4-166">Remove-AzureRmResourceLock</span></span>](./Remove-AzureRmResourceLock.md)

[<span data-ttu-id="9d3b4-167">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="9d3b4-167">Set-AzureRmResourceLock</span></span>](./Set-AzureRmResourceLock.md)


