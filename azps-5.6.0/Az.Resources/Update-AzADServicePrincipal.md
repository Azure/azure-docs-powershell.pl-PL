---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/update-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADServicePrincipal.md
ms.openlocfilehash: 44091f612720851a0ab13d54716f441d73a04065
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999793"
---
# <span data-ttu-id="f7b82-101">Update-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="f7b82-101">Update-AzADServicePrincipal</span></span>

## <span data-ttu-id="f7b82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7b82-102">SYNOPSIS</span></span>
<span data-ttu-id="f7b82-103">Aktualizuje istniejącą jednostkę zabezpieczeń usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f7b82-103">Updates an existing azure active directory service principal.</span></span>

## <span data-ttu-id="f7b82-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f7b82-104">SYNTAX</span></span>

### <span data-ttu-id="f7b82-105">SpObjectIdWithDisplayNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="f7b82-105">SpObjectIdWithDisplayNameParameterSet (Default)</span></span>
```
Update-AzADServicePrincipal -ObjectId <String> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7b82-106">SpApplicationIdWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7b82-106">SpApplicationIdWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -ApplicationId <Guid> [-Homepage <String>] [-IdentifierUri <String[]>]
 [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7b82-107">SPNWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7b82-107">SPNWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -ServicePrincipalName <String> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7b82-108">InputObjectWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7b82-108">InputObjectWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -InputObject <PSADServicePrincipal> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7b82-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="f7b82-109">DESCRIPTION</span></span>
<span data-ttu-id="f7b82-110">Aktualizuje istniejącą jednostkę zabezpieczeń usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f7b82-110">Updates an existing azure active directory service principal.</span></span> <span data-ttu-id="f7b82-111">Aby zaktualizować poświadczenia skojarzone z tym podmiotem zabezpieczeń usługi, użyj New-AzADSpCredential cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7b82-111">To update the credentials associated with this service principal, please use New-AzADSpCredential cmdlet.</span></span> <span data-ttu-id="f7b82-112">Aby zaktualizować właściwości skojarzone z aplikacją bazową, użyj Update-AzADApplication cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7b82-112">To update the properties associated with the underlying application, please use Update-AzADApplication cmdlet.</span></span>

## <span data-ttu-id="f7b82-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f7b82-113">EXAMPLES</span></span>

### <span data-ttu-id="f7b82-114">Przykład 1. Aktualizowanie nazwy wyświetlanej podmiotu zabezpieczeń usługi</span><span class="sxs-lookup"><span data-stu-id="f7b82-114">Example 1: Update the display name of a service principal</span></span>

```powershell
PS C:\> Update-AzADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 -DisplayName MyNewDisplayName
```

<span data-ttu-id="f7b82-115">Aktualizuje nazwę wyświetlaną podmiotu zabezpieczeń usługi o identyfikatorze obiektu "784136ca-3ae2-4fdd-a388-89d793e7c780" na "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="f7b82-115">Updates the display name of the service principal with object id '784136ca-3ae2-4fdd-a388-89d793e7c780' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="f7b82-116">Przykład 2. Aktualizowanie nazwy wyświetlanej podmiotu zabezpieczeń usługi za pomocą funkcji pipingu</span><span class="sxs-lookup"><span data-stu-id="f7b82-116">Example 2: Update the display name of a service principal using piping</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 | Update-AzADServicePrincipal -DisplayName MyNewDisplayName
```

<span data-ttu-id="f7b82-117">Pobiera podmiot zabezpieczeń usługi o identyfikatorze obiektu "784136ca-3ae2-4fdd-a388-89d793e7c780" i potoki, które do polecenia cmdlet programu Update-AzADServicePrincipal są przekierowywane w celu zaktualizowania nazwy wyświetlanej podmiotu zabezpieczeń usługi na "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="f7b82-117">Gets the service principal with object id '784136ca-3ae2-4fdd-a388-89d793e7c780' and pipes that to the Update-AzADServicePrincipal cmdlet to update the display name of the service principal to "MyNewDisplayName".</span></span>

### <span data-ttu-id="f7b82-118">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="f7b82-118">Example 3</span></span>

<span data-ttu-id="f7b82-119">Aktualizuje istniejącą jednostkę zabezpieczeń usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f7b82-119">Updates an existing azure active directory service principal.</span></span> <span data-ttu-id="f7b82-120">(wygenerowane automatycznie)</span><span class="sxs-lookup"><span data-stu-id="f7b82-120">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Update-AzADServicePrincipal -IdentifierUri https://mySecretApp1 -ObjectId 00000000-0000-0000-0000-00000000000000000
```

## <span data-ttu-id="f7b82-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f7b82-121">PARAMETERS</span></span>

### <span data-ttu-id="f7b82-122">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="f7b82-122">-ApplicationId</span></span>
<span data-ttu-id="f7b82-123">Identyfikator aplikacji podmiotu zabezpieczeń usługi do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="f7b82-123">The application id of the service principal to update.</span></span>

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

### <span data-ttu-id="f7b82-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7b82-124">-DefaultProfile</span></span>
<span data-ttu-id="f7b82-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f7b82-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7b82-126">— DisplayName</span><span class="sxs-lookup"><span data-stu-id="f7b82-126">-DisplayName</span></span>
<span data-ttu-id="f7b82-127">Nazwa wyświetlana podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="f7b82-127">The display name for the service principal.</span></span>

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

### <span data-ttu-id="f7b82-128">— Strona główna</span><span class="sxs-lookup"><span data-stu-id="f7b82-128">-Homepage</span></span>
<span data-ttu-id="f7b82-129">Strona główna podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="f7b82-129">The homepage for the service principal.</span></span>

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

### <span data-ttu-id="f7b82-130">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="f7b82-130">-IdentifierUri</span></span>
<span data-ttu-id="f7b82-131">Identyfikatory URI identyfikatora podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="f7b82-131">The identifier URI(s) for the service principal.</span></span>

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

### <span data-ttu-id="f7b82-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f7b82-132">-InputObject</span></span>
<span data-ttu-id="f7b82-133">Obiekt reprezentujący podmiot zabezpieczeń usługi do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="f7b82-133">The object representing the service principal to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal
Parameter Sets: InputObjectWithDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f7b82-134">-KeyCredential</span><span class="sxs-lookup"><span data-stu-id="f7b82-134">-KeyCredential</span></span>
<span data-ttu-id="f7b82-135">Poświadczenia klucza podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="f7b82-135">The key credential(s) for the service principal.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Models.KeyCredential[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7b82-136">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="f7b82-136">-ObjectId</span></span>
<span data-ttu-id="f7b82-137">Identyfikator obiektu podmiotu zabezpieczeń usługi do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="f7b82-137">The object id of the service principal to update.</span></span>

```yaml
Type: System.String
Parameter Sets: SpObjectIdWithDisplayNameParameterSet
Aliases: ServicePrincipalObjectId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7b82-138">- PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="f7b82-138">-PasswordCredential</span></span>
<span data-ttu-id="f7b82-139">Poświadczenia hasła podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="f7b82-139">The password credential(s) for the service principal.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Models.PasswordCredential[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7b82-140">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="f7b82-140">-ServicePrincipalName</span></span>
<span data-ttu-id="f7b82-141">SpN podmiotu zabezpieczeń usługi do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="f7b82-141">The SPN of the service principal to update.</span></span>

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

### <span data-ttu-id="f7b82-142">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f7b82-142">-Confirm</span></span>
<span data-ttu-id="f7b82-143">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f7b82-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7b82-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7b82-144">-WhatIf</span></span>
<span data-ttu-id="f7b82-145">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7b82-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7b82-146">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f7b82-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7b82-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7b82-147">CommonParameters</span></span>
<span data-ttu-id="f7b82-148">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7b82-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7b82-149">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f7b82-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7b82-150">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f7b82-150">INPUTS</span></span>

### <span data-ttu-id="f7b82-151">System.String</span><span class="sxs-lookup"><span data-stu-id="f7b82-151">System.String</span></span>

### <span data-ttu-id="f7b82-152">System.Guid</span><span class="sxs-lookup"><span data-stu-id="f7b82-152">System.Guid</span></span>

### <span data-ttu-id="f7b82-153">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="f7b82-153">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="f7b82-154">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f7b82-154">OUTPUTS</span></span>

### <span data-ttu-id="f7b82-155">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="f7b82-155">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="f7b82-156">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f7b82-156">NOTES</span></span>

## <span data-ttu-id="f7b82-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f7b82-157">RELATED LINKS</span></span>