---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C61FA834-BEBE-4DBF-888F-C6CB8CC95390
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADAppCredential.md
ms.openlocfilehash: f6344590828663a0cf44d96d6fe733adff8757c5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191226"
---
# <span data-ttu-id="e1bf9-101">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="e1bf9-101">Remove-AzADAppCredential</span></span>

## <span data-ttu-id="e1bf9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1bf9-102">SYNOPSIS</span></span>
<span data-ttu-id="e1bf9-103">Usuwa poświadczenia z aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e1bf9-103">Removes a credential from an application.</span></span>

## <span data-ttu-id="e1bf9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e1bf9-104">SYNTAX</span></span>

### <span data-ttu-id="e1bf9-105">ApplicationObjectIdWithKeyIdParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="e1bf9-105">ApplicationObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzADAppCredential -ObjectId <String> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1bf9-106">ApplicationIdWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1bf9-106">ApplicationIdWithKeyIdParameterSet</span></span>
```
Remove-AzADAppCredential -ApplicationId <Guid> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1bf9-107">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1bf9-107">ApplicationDisplayNameParameterSet</span></span>
```
Remove-AzADAppCredential -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1bf9-108">ApplicationObjectWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1bf9-108">ApplicationObjectWithKeyIdParameterSet</span></span>
```
Remove-AzADAppCredential [-KeyId <Guid>] -ApplicationObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1bf9-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="e1bf9-109">DESCRIPTION</span></span>
<span data-ttu-id="e1bf9-110">To Remove-AzADAppCredential cmdlet może służyć do usuwania klucza poświadczeń z aplikacji w przypadku naruszenia zabezpieczeń lub w ramach wygasania klucza poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="e1bf9-110">The Remove-AzADAppCredential cmdlet can be used to remove a credential key from an application in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="e1bf9-111">Aplikacja jest identyfikowana przez podanie identyfikatora obiektu lub identyfikatora aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e1bf9-111">The application is identified by supplying either the object ID or AppId.</span></span>
<span data-ttu-id="e1bf9-112">Poświadczenia do usunięcia są identyfikowane za pomocą identyfikatora klucza.</span><span class="sxs-lookup"><span data-stu-id="e1bf9-112">The credential to be removed is identified by its key ID.</span></span>

## <span data-ttu-id="e1bf9-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e1bf9-113">EXAMPLES</span></span>

### <span data-ttu-id="e1bf9-114">Przykład 1. Usuwanie określonego poświadczenia z aplikacji</span><span class="sxs-lookup"><span data-stu-id="e1bf9-114">Example 1: Remove a specific credential from an application</span></span>

```powershell
PS C:\> Remove-AzADAppCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="e1bf9-115">Usuwa poświadczenia o identyfikatorze klucza "9044423a-60a3-45ac-9ab1-09534157ebb" z aplikacji o identyfikatorze obiektu '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82'.</span><span class="sxs-lookup"><span data-stu-id="e1bf9-115">Removes the credential with key id '9044423a-60a3-45ac-9ab1-09534157ebb' from the application with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82'.</span></span>

### <span data-ttu-id="e1bf9-116">Przykład 2. Usuwanie wszystkich poświadczeń z aplikacji</span><span class="sxs-lookup"><span data-stu-id="e1bf9-116">Example 2: Remove all credentials from an application</span></span>

```powershell
PS C:\> Remove-AzADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58
```

<span data-ttu-id="e1bf9-117">Usuwa wszystkie poświadczenia z aplikacji o identyfikatorze aplikacji '4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58'.</span><span class="sxs-lookup"><span data-stu-id="e1bf9-117">Removes all credentials from the application with application id '4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58'.</span></span>

### <span data-ttu-id="e1bf9-118">Przykład 3. Usuwanie wszystkich poświadczeń za pomocą rur</span><span class="sxs-lookup"><span data-stu-id="e1bf9-118">Example 3: Remove all credentials using piping</span></span>

```powershell
PS C:\> Get-AzADApplication -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 | Remove-AzADAppCredential
```

<span data-ttu-id="e1bf9-119">Pobiera aplikację z identyfikatorem obiektu '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82" i potokami, które są do polecenia cmdlet programu Remove-AzADAppCredential, i usuwa wszystkie poświadczenia z tej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e1bf9-119">Gets the application with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82' and pipes that to the Remove-AzADAppCredential cmdlet and removes all credentials from that application.</span></span>

## <span data-ttu-id="e1bf9-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e1bf9-120">PARAMETERS</span></span>

### <span data-ttu-id="e1bf9-121">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="e1bf9-121">-ApplicationId</span></span>
<span data-ttu-id="e1bf9-122">Identyfikator aplikacji, z których mają być usuwane poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="e1bf9-122">The id of the application to remove the credentials from.</span></span>

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

### <span data-ttu-id="e1bf9-123">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="e1bf9-123">-ApplicationObject</span></span>
<span data-ttu-id="e1bf9-124">Obiekt aplikacji, z który mają być usuwane poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="e1bf9-124">The application object to remove the credentials from.</span></span>

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

### <span data-ttu-id="e1bf9-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1bf9-125">-DefaultProfile</span></span>
<span data-ttu-id="e1bf9-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="e1bf9-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e1bf9-127">— DisplayName</span><span class="sxs-lookup"><span data-stu-id="e1bf9-127">-DisplayName</span></span>
<span data-ttu-id="e1bf9-128">Nazwa wyświetlana aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e1bf9-128">The display name of the application.</span></span>

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

### <span data-ttu-id="e1bf9-129">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="e1bf9-129">-Force</span></span>
<span data-ttu-id="e1bf9-130">Przełącz się, aby usunąć poświadczenia bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="e1bf9-130">Switch to delete credential without a confirmation.</span></span>

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

### <span data-ttu-id="e1bf9-131">-KeyId</span><span class="sxs-lookup"><span data-stu-id="e1bf9-131">-KeyId</span></span>
<span data-ttu-id="e1bf9-132">Określa klucz poświadczeń do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="e1bf9-132">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="e1bf9-133">Identyfikatory klucza aplikacji można uzyskać za pomocą Get-AzADAppCredential cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1bf9-133">The key Ids for the application can be obtained using the Get-AzADAppCredential cmdlet.</span></span>

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

### <span data-ttu-id="e1bf9-134">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="e1bf9-134">-ObjectId</span></span>
<span data-ttu-id="e1bf9-135">Identyfikator obiektu aplikacji, z których mają być usuwane poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="e1bf9-135">The object id of the application to remove the credentials from.</span></span>

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

### <span data-ttu-id="e1bf9-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e1bf9-136">-PassThru</span></span>
<span data-ttu-id="e1bf9-137">Określenie tej wartości spowoduje zwrócenie wartości prawda, jeśli polecenie zostało pomyślnie określone.</span><span class="sxs-lookup"><span data-stu-id="e1bf9-137">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="e1bf9-138">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e1bf9-138">-Confirm</span></span>
<span data-ttu-id="e1bf9-139">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e1bf9-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1bf9-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1bf9-140">-WhatIf</span></span>
<span data-ttu-id="e1bf9-141">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1bf9-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1bf9-142">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e1bf9-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1bf9-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1bf9-143">CommonParameters</span></span>
<span data-ttu-id="e1bf9-144">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1bf9-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1bf9-145">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e1bf9-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1bf9-146">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e1bf9-146">INPUTS</span></span>

### <span data-ttu-id="e1bf9-147">System.String</span><span class="sxs-lookup"><span data-stu-id="e1bf9-147">System.String</span></span>

### <span data-ttu-id="e1bf9-148">System.Guid</span><span class="sxs-lookup"><span data-stu-id="e1bf9-148">System.Guid</span></span>

### <span data-ttu-id="e1bf9-149">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="e1bf9-149">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="e1bf9-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e1bf9-150">OUTPUTS</span></span>

### <span data-ttu-id="e1bf9-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e1bf9-151">System.Boolean</span></span>

## <span data-ttu-id="e1bf9-152">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e1bf9-152">NOTES</span></span>

## <span data-ttu-id="e1bf9-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e1bf9-153">RELATED LINKS</span></span>

[<span data-ttu-id="e1bf9-154">Get-AzadAppCredential</span><span class="sxs-lookup"><span data-stu-id="e1bf9-154">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="e1bf9-155">New-AzadAppCredential</span><span class="sxs-lookup"><span data-stu-id="e1bf9-155">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="e1bf9-156">Get-AzadApplication</span><span class="sxs-lookup"><span data-stu-id="e1bf9-156">Get-AzADApplication</span></span>](./Get-AzADApplication.md)
