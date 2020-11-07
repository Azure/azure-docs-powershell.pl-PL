---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C61FA834-BEBE-4DBF-888F-C6CB8CC95390
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADAppCredential.md
ms.openlocfilehash: 464f58a71f40315663fe5cd998c0818961c3b2fb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93895013"
---
# <span data-ttu-id="a1755-101">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="a1755-101">Remove-AzADAppCredential</span></span>

## <span data-ttu-id="a1755-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a1755-102">SYNOPSIS</span></span>
<span data-ttu-id="a1755-103">Usuwa poświadczenie z aplikacji.</span><span class="sxs-lookup"><span data-stu-id="a1755-103">Removes a credential from an application.</span></span>

## <span data-ttu-id="a1755-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a1755-104">SYNTAX</span></span>

### <span data-ttu-id="a1755-105">ApplicationObjectIdWithKeyIdParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a1755-105">ApplicationObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzADAppCredential -ObjectId <String> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1755-106">ApplicationIdWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1755-106">ApplicationIdWithKeyIdParameterSet</span></span>
```
Remove-AzADAppCredential -ApplicationId <Guid> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1755-107">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1755-107">ApplicationDisplayNameParameterSet</span></span>
```
Remove-AzADAppCredential -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1755-108">ApplicationObjectWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1755-108">ApplicationObjectWithKeyIdParameterSet</span></span>
```
Remove-AzADAppCredential [-KeyId <Guid>] -ApplicationObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1755-109">Opis</span><span class="sxs-lookup"><span data-stu-id="a1755-109">DESCRIPTION</span></span>
<span data-ttu-id="a1755-110">Polecenia cmdlet Remove-AzADAppCredential można użyć w celu usunięcia klucza poświadczeń z aplikacji w przypadku złamania zabezpieczeń lub w ramach wygaśnięcia klucza poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="a1755-110">The Remove-AzADAppCredential cmdlet can be used to remove a credential key from an application in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="a1755-111">Aplikacja jest identyfikowana przez podanie identyfikatora obiektu lub identyfikatora aplikacji.</span><span class="sxs-lookup"><span data-stu-id="a1755-111">The application is identified by supplying either the object ID or AppId.</span></span>
<span data-ttu-id="a1755-112">Poświadczenie, które ma zostać usunięte, jest identyfikowane za pomocą identyfikatora klucza.</span><span class="sxs-lookup"><span data-stu-id="a1755-112">The credential to be removed is identified by its key ID.</span></span>

## <span data-ttu-id="a1755-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a1755-113">EXAMPLES</span></span>

### <span data-ttu-id="a1755-114">Przykład 1 — Usuwanie konkretnego poświadczenia z aplikacji</span><span class="sxs-lookup"><span data-stu-id="a1755-114">Example 1 - Remove a specific credential from an application</span></span>

```
PS C:\> Remove-AzADAppCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="a1755-115">Usuwa poświadczenie o identyfikatorze klucza "9044423a-60a3-45ac-9ab1-09534157ebb" z aplikacji z identyfikatorem obiektu "7663d3fb-6f86-4352-9E6D-cf9d50d5ee82".</span><span class="sxs-lookup"><span data-stu-id="a1755-115">Removes the credential with key id '9044423a-60a3-45ac-9ab1-09534157ebb' from the application with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82'.</span></span>

### <span data-ttu-id="a1755-116">Przykład 2 — Usuwanie wszystkich poświadczeń z aplikacji</span><span class="sxs-lookup"><span data-stu-id="a1755-116">Example 2 - Remove all credentials from an application</span></span>

```
PS C:\> Remove-AzADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58
```

<span data-ttu-id="a1755-117">Usuwa wszystkie poświadczenia z aplikacji z identyfikatorem aplikacji "4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58".</span><span class="sxs-lookup"><span data-stu-id="a1755-117">Removes all credentials from the application with application id '4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58'.</span></span>

### <span data-ttu-id="a1755-118">Przykład 3-Usuwanie wszystkich poświadczeń przy użyciu połączeń rurowych</span><span class="sxs-lookup"><span data-stu-id="a1755-118">Example 3 - Remove all credentials using piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 | Remove-AzADAppCredential
```

<span data-ttu-id="a1755-119">Pobiera aplikację o identyfikatorze obiektu "7663d3fb-6f86-4352-9E6D-cf9d50d5ee82" i potokach, które zostaną usunięte przez polecenie cmdlet Remove-AzADAppCredential i usuwa wszystkie poświadczenia z tej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="a1755-119">Gets the application with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82' and pipes that to the Remove-AzADAppCredential cmdlet and removes all credentials from that application.</span></span>

## <span data-ttu-id="a1755-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a1755-120">PARAMETERS</span></span>

### <span data-ttu-id="a1755-121">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="a1755-121">-ApplicationId</span></span>
<span data-ttu-id="a1755-122">Identyfikator aplikacji, z której mają zostać usunięte poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="a1755-122">The id of the application to remove the credentials from.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1755-123">-Applicationobject</span><span class="sxs-lookup"><span data-stu-id="a1755-123">-ApplicationObject</span></span>
<span data-ttu-id="a1755-124">Obiekt aplikacji, z którego mają zostać usunięte poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="a1755-124">The application object to remove the credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1755-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1755-125">-DefaultProfile</span></span>
<span data-ttu-id="a1755-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="a1755-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a1755-127">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a1755-127">-DisplayName</span></span>
<span data-ttu-id="a1755-128">Nazwa wyświetlana aplikacji.</span><span class="sxs-lookup"><span data-stu-id="a1755-128">The display name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1755-129">-Force</span><span class="sxs-lookup"><span data-stu-id="a1755-129">-Force</span></span>
<span data-ttu-id="a1755-130">Przełączanie do usuwania poświadczenia bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="a1755-130">Switch to delete credential without a confirmation.</span></span>

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

### <span data-ttu-id="a1755-131">-KeyId</span><span class="sxs-lookup"><span data-stu-id="a1755-131">-KeyId</span></span>
<span data-ttu-id="a1755-132">Określa klucz poświadczenia, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="a1755-132">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="a1755-133">Identyfikatory kluczy aplikacji można uzyskać przy użyciu polecenia cmdlet Get-AzADAppCredential.</span><span class="sxs-lookup"><span data-stu-id="a1755-133">The key Ids for the application can be obtained using the Get-AzADAppCredential cmdlet.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectIdWithKeyIdParameterSet, ApplicationIdWithKeyIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectWithKeyIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1755-134">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="a1755-134">-ObjectId</span></span>
<span data-ttu-id="a1755-135">Identyfikator obiektu aplikacji, z którego mają zostać usunięte poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="a1755-135">The object id of the application to remove the credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1755-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a1755-136">-PassThru</span></span>
<span data-ttu-id="a1755-137">Określenie tej wartości zwróci wartość PRAWDA, jeśli polecenie zostało wykonane prawidłowo.</span><span class="sxs-lookup"><span data-stu-id="a1755-137">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="a1755-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a1755-138">-Confirm</span></span>
<span data-ttu-id="a1755-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1755-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1755-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1755-140">-WhatIf</span></span>
<span data-ttu-id="a1755-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1755-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1755-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a1755-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1755-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1755-143">CommonParameters</span></span>
<span data-ttu-id="a1755-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1755-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1755-145">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a1755-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1755-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a1755-146">INPUTS</span></span>

### <span data-ttu-id="a1755-147">System. String</span><span class="sxs-lookup"><span data-stu-id="a1755-147">System.String</span></span>

### <span data-ttu-id="a1755-148">System. GUID</span><span class="sxs-lookup"><span data-stu-id="a1755-148">System.Guid</span></span>

### <span data-ttu-id="a1755-149">Microsoft. Azure. Commands. pozycji. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="a1755-149">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="a1755-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a1755-150">OUTPUTS</span></span>

### <span data-ttu-id="a1755-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a1755-151">System.Boolean</span></span>

## <span data-ttu-id="a1755-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a1755-152">NOTES</span></span>

## <span data-ttu-id="a1755-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a1755-153">RELATED LINKS</span></span>

[<span data-ttu-id="a1755-154">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="a1755-154">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="a1755-155">Nowe — AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="a1755-155">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="a1755-156">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="a1755-156">Get-AzADApplication</span></span>](./Get-AzADApplication.md)
