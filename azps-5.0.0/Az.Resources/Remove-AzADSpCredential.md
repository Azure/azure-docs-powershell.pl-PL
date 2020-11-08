---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 04B1E3A6-6D52-46A3-8241-2CCDB5E71642
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADSpCredential.md
ms.openlocfilehash: bcb33f87b85eb6ad5bce9ba812ebccb4d154e920
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224848"
---
# <span data-ttu-id="ef74a-101">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="ef74a-101">Remove-AzADSpCredential</span></span>

## <span data-ttu-id="ef74a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ef74a-102">SYNOPSIS</span></span>
<span data-ttu-id="ef74a-103">Usuwa poświadczenia z podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="ef74a-103">Removes a credential from a service principal.</span></span>

## <span data-ttu-id="ef74a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ef74a-104">SYNTAX</span></span>

### <span data-ttu-id="ef74a-105">ObjectIdWithKeyIdParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ef74a-105">ObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzADSpCredential -ObjectId <String> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef74a-106">SPNWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef74a-106">SPNWithKeyIdParameterSet</span></span>
```
Remove-AzADSpCredential -ServicePrincipalName <String> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef74a-107">DisplayNameWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef74a-107">DisplayNameWithKeyIdParameterSet</span></span>
```
Remove-AzADSpCredential -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef74a-108">ServicePrincipalObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef74a-108">ServicePrincipalObjectParameterSet</span></span>
```
Remove-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef74a-109">Opis</span><span class="sxs-lookup"><span data-stu-id="ef74a-109">DESCRIPTION</span></span>
<span data-ttu-id="ef74a-110">Polecenia cmdlet Remove-AzADSpCredential można użyć w celu usunięcia klucza poświadczeń z podmiotu zabezpieczeń usługi w przypadku złamania zabezpieczeń lub jako część wygaśnięcia przerzucania klucza poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="ef74a-110">The Remove-AzADSpCredential cmdlet can be used to remove a credential key from a service principal in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="ef74a-111">Wartość główna usługi jest identyfikowana przez podanie identyfikatora obiektu lub głównej nazwy usługi (SPN).</span><span class="sxs-lookup"><span data-stu-id="ef74a-111">The service principal is identified by supplying either the object ID or service principal name (SPN).</span></span>
<span data-ttu-id="ef74a-112">Poświadczenie, które ma zostać usunięte, jest identyfikowane przez identyfikator klucza, jeśli pojedyncze poświadczenie ma zostać usunięte lub z przełącznikiem wszystkie, aby usunąć wszystkie poświadczenia skojarzone z podmiotem zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="ef74a-112">The credential to be removed is identified by its key ID if an individual credential is to be removed or with an 'All' switch to delete all credentials associated with the service principal.</span></span>

## <span data-ttu-id="ef74a-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ef74a-113">EXAMPLES</span></span>

### <span data-ttu-id="ef74a-114">Przykład 1: usuwanie konkretnego poświadczenia z podmiotu zabezpieczeń usługi</span><span class="sxs-lookup"><span data-stu-id="ef74a-114">Example 1: Remove a specific credential from a service principal</span></span>

```powershell
PS C:\> Remove-AzADSpCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="ef74a-115">Usuwa poświadczenie o identyfikatorze klucza "9044423a-60a3-45ac-9ab1-09534157ebb" z podmiotu zabezpieczeń usługi z identyfikatorem obiektu "7663d3fb-6f86-4352-9E6D-cf9d50d5ee82".</span><span class="sxs-lookup"><span data-stu-id="ef74a-115">Removes the credential with key id '9044423a-60a3-45ac-9ab1-09534157ebb' from the service principal with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82'.</span></span>

### <span data-ttu-id="ef74a-116">Przykład 2: Usuwanie wszystkich poświadczeń z podmiotu zabezpieczeń usługi</span><span class="sxs-lookup"><span data-stu-id="ef74a-116">Example 2: Remove all credentials from a service principal</span></span>

```powershell
PS C:\> Remove-AzADSpCredential -ServicePrincipalName http://test123
```

<span data-ttu-id="ef74a-117">Usuwa wszystkie poświadczenia podmiotu zabezpieczeń usługi z główną nazwę użytkownika " http://test123 ".</span><span class="sxs-lookup"><span data-stu-id="ef74a-117">Removes all credentials from the service principal with the SPN "http://test123".</span></span>

### <span data-ttu-id="ef74a-118">Przykład 3: Usuwanie wszystkich poświadczeń z podmiotu zabezpieczeń usługi przy użyciu połączeń rurowych</span><span class="sxs-lookup"><span data-stu-id="ef74a-118">Example 3: Remove all credentials from a service principal using piping</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 | Remove-AzADSpCredential
```

<span data-ttu-id="ef74a-119">Pobiera podmiot zabezpieczeń usługi o identyfikatorze obiektu "7663d3fb-6f86-4352-9E6D-cf9d50d5ee82" i potokach, które zostaną usunięte przez polecenie cmdlet Remove-AzADSpCredential, aby usunąć wszystkie poświadczenia tego podmiotu usługi.</span><span class="sxs-lookup"><span data-stu-id="ef74a-119">Gets the service principal with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82' and pipes that to the Remove-AzADSpCredential cmdlet to remove all credentials from that service principal.</span></span>

## <span data-ttu-id="ef74a-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ef74a-120">PARAMETERS</span></span>

### <span data-ttu-id="ef74a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef74a-121">-DefaultProfile</span></span>
<span data-ttu-id="ef74a-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="ef74a-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ef74a-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ef74a-123">-DisplayName</span></span>
<span data-ttu-id="ef74a-124">Nazwa wyświetlana podmiotu usługi.</span><span class="sxs-lookup"><span data-stu-id="ef74a-124">The display name of the service principal.</span></span>

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

### <span data-ttu-id="ef74a-125">-Force</span><span class="sxs-lookup"><span data-stu-id="ef74a-125">-Force</span></span>
<span data-ttu-id="ef74a-126">Przełączanie do usuwania poświadczenia bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="ef74a-126">Switch to delete credential without a confirmation.</span></span>

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

### <span data-ttu-id="ef74a-127">-KeyId</span><span class="sxs-lookup"><span data-stu-id="ef74a-127">-KeyId</span></span>
<span data-ttu-id="ef74a-128">Określa klucz poświadczenia, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="ef74a-128">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="ef74a-129">Identyfikatory kluczy dla podmiotu usługi można uzyskać przy użyciu polecenia cmdlet Get-AzADSpCredential.</span><span class="sxs-lookup"><span data-stu-id="ef74a-129">The key Ids for a service principal can be obtained using the Get-AzADSpCredential cmdlet.</span></span>

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

### <span data-ttu-id="ef74a-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="ef74a-130">-ObjectId</span></span>
<span data-ttu-id="ef74a-131">Identyfikator obiektu podmiotu usługi, z którego mają zostać usunięte poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="ef74a-131">The object id of the service principal to remove the credentials from.</span></span>

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

### <span data-ttu-id="ef74a-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ef74a-132">-PassThru</span></span>
<span data-ttu-id="ef74a-133">Określenie tej wartości zwróci wartość PRAWDA, jeśli polecenie zostało wykonane prawidłowo.</span><span class="sxs-lookup"><span data-stu-id="ef74a-133">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="ef74a-134">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="ef74a-134">-ServicePrincipalName</span></span>
<span data-ttu-id="ef74a-135">Nazwa (SPN) podmiotu usługi, z którego mają zostać usunięte poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="ef74a-135">The name (SPN) of the service principal to remove the credentials from.</span></span>

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

### <span data-ttu-id="ef74a-136">-Serviceprincipalobject</span><span class="sxs-lookup"><span data-stu-id="ef74a-136">-ServicePrincipalObject</span></span>
<span data-ttu-id="ef74a-137">Obiekt główny usługi, z którego mają zostać usunięte poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="ef74a-137">The service principal object to remove the credentials from.</span></span>

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

### <span data-ttu-id="ef74a-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ef74a-138">-Confirm</span></span>
<span data-ttu-id="ef74a-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef74a-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef74a-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef74a-140">-WhatIf</span></span>
<span data-ttu-id="ef74a-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef74a-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef74a-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ef74a-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef74a-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef74a-143">CommonParameters</span></span>
<span data-ttu-id="ef74a-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef74a-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef74a-145">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ef74a-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef74a-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ef74a-146">INPUTS</span></span>

### <span data-ttu-id="ef74a-147">System. String</span><span class="sxs-lookup"><span data-stu-id="ef74a-147">System.String</span></span>

### <span data-ttu-id="ef74a-148">Microsoft. Azure. Commands. pozycji. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="ef74a-148">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="ef74a-149">System. GUID</span><span class="sxs-lookup"><span data-stu-id="ef74a-149">System.Guid</span></span>

## <span data-ttu-id="ef74a-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ef74a-150">OUTPUTS</span></span>

### <span data-ttu-id="ef74a-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ef74a-151">System.Boolean</span></span>

## <span data-ttu-id="ef74a-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ef74a-152">NOTES</span></span>

## <span data-ttu-id="ef74a-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ef74a-153">RELATED LINKS</span></span>

[<span data-ttu-id="ef74a-154">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="ef74a-154">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="ef74a-155">Nowe — AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="ef74a-155">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="ef74a-156">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="ef74a-156">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

