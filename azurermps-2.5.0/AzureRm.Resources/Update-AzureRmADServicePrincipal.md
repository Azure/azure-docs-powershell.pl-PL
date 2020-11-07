---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/update-azurermadserviceprincipal
schema: 2.0.0
ms.openlocfilehash: d3e5459c81d2abbe7178652ce7b00fc35e6e3bbd
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898173"
---
# <span data-ttu-id="2423d-101">Update-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="2423d-101">Update-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="2423d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2423d-102">SYNOPSIS</span></span>
<span data-ttu-id="2423d-103">Aktualizuje istniejącego podmiot zabezpieczeń usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2423d-103">Updates an existing azure active directory service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2423d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2423d-104">SYNTAX</span></span>

### <span data-ttu-id="2423d-105">SpObjectIdWithDisplayNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2423d-105">SpObjectIdWithDisplayNameParameterSet (Default)</span></span>
```
Update-AzureRmADServicePrincipal -ObjectId <Guid> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2423d-106">SpApplicationIdWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2423d-106">SpApplicationIdWithDisplayNameParameterSet</span></span>
```
Update-AzureRmADServicePrincipal -ApplicationId <Guid> [-Homepage <String>] [-IdentifierUri <String[]>]
 [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2423d-107">SPNWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2423d-107">SPNWithDisplayNameParameterSet</span></span>
```
Update-AzureRmADServicePrincipal -ServicePrincipalName <String> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2423d-108">InputObjectWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2423d-108">InputObjectWithDisplayNameParameterSet</span></span>
```
Update-AzureRmADServicePrincipal -InputObject <PSADServicePrincipal> [-DisplayName <String>]
 [-Homepage <String>] [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>]
 [-PasswordCredential <PasswordCredential[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2423d-109">Opis</span><span class="sxs-lookup"><span data-stu-id="2423d-109">DESCRIPTION</span></span>
<span data-ttu-id="2423d-110">Aktualizuje istniejącego podmiot zabezpieczeń usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2423d-110">Updates an existing azure active directory service principal.</span></span> <span data-ttu-id="2423d-111">Aby zaktualizować poświadczenia skojarzone z tym podmiotem usługi, użyj New-AzureRmADSpCredential polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2423d-111">To update the credentials associated with this service principal, please use New-AzureRmADSpCredential cmdlet.</span></span> <span data-ttu-id="2423d-112">Aby zaktualizować właściwości skojarzone z aplikacją podstawową, użyj polecenia cmdlet Update-AzureRmADApplication.</span><span class="sxs-lookup"><span data-stu-id="2423d-112">To update the properties associated with the underlying application, please use Update-AzureRmADApplication cmdlet.</span></span>

## <span data-ttu-id="2423d-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2423d-113">EXAMPLES</span></span>

### <span data-ttu-id="2423d-114">Przykład 1 — Aktualizowanie nazwy wyświetlanej podmiotu zabezpieczeń usługi</span><span class="sxs-lookup"><span data-stu-id="2423d-114">Example 1 - Update the display name of a service principal</span></span>

```
PS C:\> Update-AzureRmADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 -DisplayName MyNewDisplayName
```

<span data-ttu-id="2423d-115">Aktualizuje nazwę wyświetlaną podmiotu usługi o identyfikatorze obiektu "784136ca-3ae2-4fdd-a388-89d793e7c780" na "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="2423d-115">Updates the display name of the service principal with object id '784136ca-3ae2-4fdd-a388-89d793e7c780' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="2423d-116">Przykład 2 — aktualizowanie nazwy wyświetlanej podmiotu usługi przy użyciu połączeń rurowych</span><span class="sxs-lookup"><span data-stu-id="2423d-116">Example 2 - Update the display name of a service principal using piping</span></span>

```
PS C:\> Get-AzureRmADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 | Update-AzureRmADServicePrincipal -DisplayName MyNewDisplayName
```

<span data-ttu-id="2423d-117">Pobiera podmiot zabezpieczeń usługi o identyfikatorze obiektu "784136ca-3ae2-4fdd-a388-89d793e7c780" i potokach, które są wyświetlane za pomocą polecenia cmdlet Update-AzureRmADServicePrincipal, w celu zaktualizowania nazwy wyświetlanej głównego obiektu usługi na "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="2423d-117">Gets the service principal with object id '784136ca-3ae2-4fdd-a388-89d793e7c780' and pipes that to the Update-AzureRmADServicePrincipal cmdlet to update the display name of the service principal to "MyNewDisplayName".</span></span>

## <span data-ttu-id="2423d-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2423d-118">PARAMETERS</span></span>

### <span data-ttu-id="2423d-119">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="2423d-119">-ApplicationId</span></span>
<span data-ttu-id="2423d-120">Identyfikator aplikacji głównej usługi do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="2423d-120">The application id of the service principal to update.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SpApplicationIdWithDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2423d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2423d-121">-DefaultProfile</span></span>
<span data-ttu-id="2423d-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2423d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2423d-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="2423d-123">-DisplayName</span></span>
<span data-ttu-id="2423d-124">Nazwa wyświetlana podmiotu usługi.</span><span class="sxs-lookup"><span data-stu-id="2423d-124">The display name for the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: SpObjectIdWithDisplayNameParameterSet, SPNWithDisplayNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObjectWithDisplayNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2423d-125">-Strona główna</span><span class="sxs-lookup"><span data-stu-id="2423d-125">-Homepage</span></span>
<span data-ttu-id="2423d-126">Strona główna dla głównej usługi.</span><span class="sxs-lookup"><span data-stu-id="2423d-126">The homepage for the service principal.</span></span>

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

### <span data-ttu-id="2423d-127">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="2423d-127">-IdentifierUri</span></span>
<span data-ttu-id="2423d-128">Identyfikator URI identyfikatora dla podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="2423d-128">The identifier URI(s) for the service principal.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2423d-129">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2423d-129">-InputObject</span></span>
<span data-ttu-id="2423d-130">Obiekt reprezentujący podmiot zabezpieczeń usługi, który ma zostać zaktualizowany.</span><span class="sxs-lookup"><span data-stu-id="2423d-130">The object representing the service principal to update.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal
Parameter Sets: InputObjectWithDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2423d-131">-Poświadczenia</span><span class="sxs-lookup"><span data-stu-id="2423d-131">-KeyCredential</span></span>
<span data-ttu-id="2423d-132">Główne poświadczenia dla podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="2423d-132">The key credential(s) for the service principal.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.Models.KeyCredential[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2423d-133">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="2423d-133">-ObjectId</span></span>
<span data-ttu-id="2423d-134">Identyfikator obiektu podmiotu usługi do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="2423d-134">The object id of the service principal to update.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SpObjectIdWithDisplayNameParameterSet
Aliases: ServicePrincipalObjectId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2423d-135">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="2423d-135">-PasswordCredential</span></span>
<span data-ttu-id="2423d-136">Poświadczenie hasła dla podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="2423d-136">The password credential(s) for the service principal.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.Models.PasswordCredential[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2423d-137">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="2423d-137">-ServicePrincipalName</span></span>
<span data-ttu-id="2423d-138">Główna nazwa SPN usługi, która ma zostać zaktualizowana.</span><span class="sxs-lookup"><span data-stu-id="2423d-138">The SPN of the service principal to update.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNWithDisplayNameParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2423d-139">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2423d-139">-Confirm</span></span>
<span data-ttu-id="2423d-140">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2423d-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2423d-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2423d-141">-WhatIf</span></span>
<span data-ttu-id="2423d-142">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2423d-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2423d-143">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2423d-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2423d-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2423d-144">CommonParameters</span></span>
<span data-ttu-id="2423d-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2423d-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2423d-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2423d-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2423d-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2423d-147">INPUTS</span></span>

### <span data-ttu-id="2423d-148">System. GUID</span><span class="sxs-lookup"><span data-stu-id="2423d-148">System.Guid</span></span>

### <span data-ttu-id="2423d-149">System. String</span><span class="sxs-lookup"><span data-stu-id="2423d-149">System.String</span></span>

### <span data-ttu-id="2423d-150">Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="2423d-150">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>
<span data-ttu-id="2423d-151">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2423d-151">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="2423d-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2423d-152">OUTPUTS</span></span>

### <span data-ttu-id="2423d-153">Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="2423d-153">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="2423d-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2423d-154">NOTES</span></span>

## <span data-ttu-id="2423d-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2423d-155">RELATED LINKS</span></span>
