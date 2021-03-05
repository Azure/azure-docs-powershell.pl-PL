---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 04B1E3A6-6D52-46A3-8241-2CCDB5E71642
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADSpCredential.md
ms.openlocfilehash: b71a25fa7e3e7c70b363b3462294e3c071a6ce86
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970337"
---
# <span data-ttu-id="121fe-101">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="121fe-101">Remove-AzADSpCredential</span></span>

## <span data-ttu-id="121fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="121fe-102">SYNOPSIS</span></span>
<span data-ttu-id="121fe-103">Usuwa poświadczenia podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="121fe-103">Removes a credential from a service principal.</span></span>

## <span data-ttu-id="121fe-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="121fe-104">SYNTAX</span></span>

### <span data-ttu-id="121fe-105">ObjectIdWithKeyIdParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="121fe-105">ObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzADSpCredential -ObjectId <String> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="121fe-106">SPNWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="121fe-106">SPNWithKeyIdParameterSet</span></span>
```
Remove-AzADSpCredential -ServicePrincipalName <String> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="121fe-107">DisplayNameWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="121fe-107">DisplayNameWithKeyIdParameterSet</span></span>
```
Remove-AzADSpCredential -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="121fe-108">ServicePrincipalObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="121fe-108">ServicePrincipalObjectParameterSet</span></span>
```
Remove-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="121fe-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="121fe-109">DESCRIPTION</span></span>
<span data-ttu-id="121fe-110">To Remove-AzADSpCredential cmdlet może służyć do usuwania klucza poświadczeń od podmiotu zabezpieczeń usługi w przypadku naruszenia zabezpieczeń lub w ramach wygasania klucza poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="121fe-110">The Remove-AzADSpCredential cmdlet can be used to remove a credential key from a service principal in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="121fe-111">Podmiot zabezpieczeń usługi jest identyfikowany przez dostarczenie identyfikatora obiektu lub nazwy podmiotu zabezpieczeń usługi (SPN).</span><span class="sxs-lookup"><span data-stu-id="121fe-111">The service principal is identified by supplying either the object ID or service principal name (SPN).</span></span>
<span data-ttu-id="121fe-112">Usunięte poświadczenia są identyfikowane za pomocą identyfikatora klucza, jeśli pojedyncze poświadczenia mają zostać usunięte, lub przełącznikiem "Wszystko" w celu usunięcia wszystkich poświadczeń skojarzonych z podmiotem zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="121fe-112">The credential to be removed is identified by its key ID if an individual credential is to be removed or with an 'All' switch to delete all credentials associated with the service principal.</span></span>

## <span data-ttu-id="121fe-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="121fe-113">EXAMPLES</span></span>

### <span data-ttu-id="121fe-114">Przykład 1. Usunięcie określonego poświadczenia podmiotu zabezpieczeń usługi</span><span class="sxs-lookup"><span data-stu-id="121fe-114">Example 1: Remove a specific credential from a service principal</span></span>

```powershell
PS C:\> Remove-AzADSpCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="121fe-115">Usuwa poświadczenia o identyfikatorze klucza "9044423a-60a3-45ac-9ab1-09534157ebb" podmiotu zabezpieczeń usługi z identyfikatorem obiektu '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82'.</span><span class="sxs-lookup"><span data-stu-id="121fe-115">Removes the credential with key id '9044423a-60a3-45ac-9ab1-09534157ebb' from the service principal with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82'.</span></span>

### <span data-ttu-id="121fe-116">Przykład 2. Usuwanie wszystkich poświadczeń podmiotu zabezpieczeń usługi</span><span class="sxs-lookup"><span data-stu-id="121fe-116">Example 2: Remove all credentials from a service principal</span></span>

```powershell
PS C:\> Remove-AzADSpCredential -ServicePrincipalName http://test123
```

<span data-ttu-id="121fe-117">Usuwa wszystkie poświadczenia podmiotu zabezpieczeń usługi za pomocą dodatku SPN " http://test123 ".</span><span class="sxs-lookup"><span data-stu-id="121fe-117">Removes all credentials from the service principal with the SPN "http://test123".</span></span>

### <span data-ttu-id="121fe-118">Przykład 3. Usuwanie wszystkich poświadczeń podmiotu zabezpieczeń usługi za pomocą funkcji pipingu</span><span class="sxs-lookup"><span data-stu-id="121fe-118">Example 3: Remove all credentials from a service principal using piping</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 | Remove-AzADSpCredential
```

<span data-ttu-id="121fe-119">Pobiera podmiot zabezpieczeń usługi o identyfikatorze obiektu "7663d3fb-6f86-4352-9e6d-cf9d50d5ee82" i potoki, które są do polecenia cmdlet usługi Remove-AzADSpCredential w celu usunięcia wszystkich poświadczeń tego podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="121fe-119">Gets the service principal with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82' and pipes that to the Remove-AzADSpCredential cmdlet to remove all credentials from that service principal.</span></span>

## <span data-ttu-id="121fe-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="121fe-120">PARAMETERS</span></span>

### <span data-ttu-id="121fe-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="121fe-121">-DefaultProfile</span></span>
<span data-ttu-id="121fe-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="121fe-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="121fe-123">— DisplayName</span><span class="sxs-lookup"><span data-stu-id="121fe-123">-DisplayName</span></span>
<span data-ttu-id="121fe-124">Nazwa wyświetlana podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="121fe-124">The display name of the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="121fe-125">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="121fe-125">-Force</span></span>
<span data-ttu-id="121fe-126">Przełącz się, aby usunąć poświadczenia bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="121fe-126">Switch to delete credential without a confirmation.</span></span>

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

### <span data-ttu-id="121fe-127">-KeyId</span><span class="sxs-lookup"><span data-stu-id="121fe-127">-KeyId</span></span>
<span data-ttu-id="121fe-128">Określa klucz poświadczeń do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="121fe-128">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="121fe-129">Identyfikatory klucza podmiotu zabezpieczeń usługi można uzyskać za pomocą Get-AzADSpCredential cmdlet.</span><span class="sxs-lookup"><span data-stu-id="121fe-129">The key Ids for a service principal can be obtained using the Get-AzADSpCredential cmdlet.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdWithKeyIdParameterSet, SPNWithKeyIdParameterSet, ServicePrincipalObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="121fe-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="121fe-130">-ObjectId</span></span>
<span data-ttu-id="121fe-131">Identyfikator obiektu podmiotu zabezpieczeń usługi do usunięcia poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="121fe-131">The object id of the service principal to remove the credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="121fe-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="121fe-132">-PassThru</span></span>
<span data-ttu-id="121fe-133">Określenie tej wartości spowoduje zwrócenie wartości prawda, jeśli polecenie zostało pomyślnie określone.</span><span class="sxs-lookup"><span data-stu-id="121fe-133">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="121fe-134">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="121fe-134">-ServicePrincipalName</span></span>
<span data-ttu-id="121fe-135">Nazwa (SPN) podmiotu zabezpieczeń usługi, z których mają być usuwane poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="121fe-135">The name (SPN) of the service principal to remove the credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="121fe-136">-ServicePrincipalObject</span><span class="sxs-lookup"><span data-stu-id="121fe-136">-ServicePrincipalObject</span></span>
<span data-ttu-id="121fe-137">Obiekt podmiotu zabezpieczeń usługi, z który mają być usuwane poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="121fe-137">The service principal object to remove the credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal
Parameter Sets: ServicePrincipalObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="121fe-138">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="121fe-138">-Confirm</span></span>
<span data-ttu-id="121fe-139">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="121fe-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="121fe-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="121fe-140">-WhatIf</span></span>
<span data-ttu-id="121fe-141">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="121fe-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="121fe-142">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="121fe-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="121fe-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="121fe-143">CommonParameters</span></span>
<span data-ttu-id="121fe-144">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="121fe-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="121fe-145">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="121fe-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="121fe-146">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="121fe-146">INPUTS</span></span>

### <span data-ttu-id="121fe-147">System.String</span><span class="sxs-lookup"><span data-stu-id="121fe-147">System.String</span></span>

### <span data-ttu-id="121fe-148">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="121fe-148">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="121fe-149">System.Guid</span><span class="sxs-lookup"><span data-stu-id="121fe-149">System.Guid</span></span>

## <span data-ttu-id="121fe-150">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="121fe-150">OUTPUTS</span></span>

### <span data-ttu-id="121fe-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="121fe-151">System.Boolean</span></span>

## <span data-ttu-id="121fe-152">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="121fe-152">NOTES</span></span>

## <span data-ttu-id="121fe-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="121fe-153">RELATED LINKS</span></span>

[<span data-ttu-id="121fe-154">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="121fe-154">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="121fe-155">New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="121fe-155">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="121fe-156">Get-AzadServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="121fe-156">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

