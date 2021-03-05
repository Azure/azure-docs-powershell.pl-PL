---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/update-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADApplication.md
ms.openlocfilehash: 329620701c4afb52bdebd145ef461c7d311c26a2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997144"
---
# <span data-ttu-id="80a2d-101">Update-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="80a2d-101">Update-AzADApplication</span></span>

## <span data-ttu-id="80a2d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80a2d-102">SYNOPSIS</span></span>
<span data-ttu-id="80a2d-103">Aktualizuje istniejącą aplikację usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="80a2d-103">Updates an existing azure active directory application.</span></span>

## <span data-ttu-id="80a2d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="80a2d-104">SYNTAX</span></span>

### <span data-ttu-id="80a2d-105">ApplicationObjectIdWithUpdateParamsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="80a2d-105">ApplicationObjectIdWithUpdateParamsParameterSet (Default)</span></span>
```
Update-AzADApplication -ObjectId <String> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUri <String[]>] [-ReplyUrl <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80a2d-106">ApplicationIdWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="80a2d-106">ApplicationIdWithUpdateParamsParameterSet</span></span>
```
Update-AzADApplication -ApplicationId <Guid> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUri <String[]>] [-ReplyUrl <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80a2d-107">InputObjectWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="80a2d-107">InputObjectWithUpdateParamsParameterSet</span></span>
```
Update-AzADApplication -InputObject <PSADApplication> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUri <String[]>] [-ReplyUrl <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80a2d-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="80a2d-108">DESCRIPTION</span></span>
<span data-ttu-id="80a2d-109">Aktualizuje istniejącą aplikację usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="80a2d-109">Updates an existing azure active directory application.</span></span>
<span data-ttu-id="80a2d-110">Aby zaktualizować poświadczenia skojarzone z tą aplikacją, użyj New-AzADAppCredential cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80a2d-110">To update the credentials associated with this application, please use the New-AzADAppCredential cmdlet.</span></span>

## <span data-ttu-id="80a2d-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="80a2d-111">EXAMPLES</span></span>

### <span data-ttu-id="80a2d-112">Przykład 1. Aktualizowanie nazwy wyświetlanej aplikacji</span><span class="sxs-lookup"><span data-stu-id="80a2d-112">Example 1 - Update the display name of an application</span></span>

```
PS C:\> Update-AzADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName MyNewDisplayName
```

<span data-ttu-id="80a2d-113">Aktualizuje nazwę wyświetlaną aplikacji o identyfikatorze obiektu "fb7b3405-ca44-4b5b-8584-12392f5d96d7" na "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="80a2d-113">Updates the display name of the application with object id 'fb7b3405-ca44-4b5b-8584-12392f5d96d7' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="80a2d-114">Przykład 2. Aktualizowanie wszystkich właściwości aplikacji</span><span class="sxs-lookup"><span data-stu-id="80a2d-114">Example 2 - Update all properties of an application</span></span>

```
PS C:\> Update-AzADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName MyNewDisplayName -HomePage https://www.microsoft.com -IdentifierUris "https://UpdateAppUri"
```

<span data-ttu-id="80a2d-115">Aktualizuje właściwości aplikacji za pomocą identyfikatora obiektu "fb7b3405-ca44-4b5b-8584-12392f5d96d7".</span><span class="sxs-lookup"><span data-stu-id="80a2d-115">Updates the properties of an application with object id 'fb7b3405-ca44-4b5b-8584-12392f5d96d7'.</span></span>

### <span data-ttu-id="80a2d-116">Przykład 3. Aktualizowanie nazwy wyświetlanej aplikacji za pomocą rur</span><span class="sxs-lookup"><span data-stu-id="80a2d-116">Example 3 - Update the display name of an application using piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 | Update-AzADApplication -DisplayName MyNewDisplayName
```

<span data-ttu-id="80a2d-117">Pobiera aplikację o identyfikatorze obiektu "fb7b3405-ca44-4b5b-8584-12392f5d96d7" i potoki, które są do polecenia cmdlet programu Update-AzADApplication, aby zaktualizować nazwę wyświetlaną aplikacji na "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="80a2d-117">Gets the application with object id 'fb7b3405-ca44-4b5b-8584-12392f5d96d7' and pipes that to the Update-AzADApplication cmdlet to update the display name of the application to "MyNewDisplayName".</span></span>

## <span data-ttu-id="80a2d-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="80a2d-118">PARAMETERS</span></span>

### <span data-ttu-id="80a2d-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="80a2d-119">-ApplicationId</span></span>
<span data-ttu-id="80a2d-120">Identyfikator aplikacji do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="80a2d-120">The application id of the application to update.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdWithUpdateParamsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80a2d-121">-AvailableToOtherTenants</span><span class="sxs-lookup"><span data-stu-id="80a2d-121">-AvailableToOtherTenants</span></span>
<span data-ttu-id="80a2d-122">Ma wartość True (Prawda), jeśli aplikacja jest udostępniana innym dzierżawom; w przeciwnym razie fałsz.</span><span class="sxs-lookup"><span data-stu-id="80a2d-122">True if the application is shared with other tenants; otherwise, false.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet, ApplicationIdWithUpdateParamsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Boolean
Parameter Sets: InputObjectWithUpdateParamsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80a2d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80a2d-123">-DefaultProfile</span></span>
<span data-ttu-id="80a2d-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="80a2d-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80a2d-125">— DisplayName</span><span class="sxs-lookup"><span data-stu-id="80a2d-125">-DisplayName</span></span>
<span data-ttu-id="80a2d-126">Nazwa wyświetlana aplikacji do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="80a2d-126">The display name for the application to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet, ApplicationIdWithUpdateParamsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObjectWithUpdateParamsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80a2d-127">-Strona główna</span><span class="sxs-lookup"><span data-stu-id="80a2d-127">-HomePage</span></span>
<span data-ttu-id="80a2d-128">Adres URL strony głównej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="80a2d-128">The URL to the application's homepage.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet, ApplicationIdWithUpdateParamsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObjectWithUpdateParamsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80a2d-129">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="80a2d-129">-IdentifierUri</span></span>
<span data-ttu-id="80a2d-130">URI identyfikujące aplikację.</span><span class="sxs-lookup"><span data-stu-id="80a2d-130">The URIs that identify the application.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet, ApplicationIdWithUpdateParamsParameterSet
Aliases: IdentifierUris

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: InputObjectWithUpdateParamsParameterSet
Aliases: IdentifierUris

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80a2d-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="80a2d-131">-InputObject</span></span>
<span data-ttu-id="80a2d-132">Obiekt reprezentujący aplikację do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="80a2d-132">The object representing the application to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: InputObjectWithUpdateParamsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="80a2d-133">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="80a2d-133">-ObjectId</span></span>
<span data-ttu-id="80a2d-134">Identyfikator obiektu aplikacji do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="80a2d-134">The object id of the application to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80a2d-135">- ReplyUrl</span><span class="sxs-lookup"><span data-stu-id="80a2d-135">-ReplyUrl</span></span>
<span data-ttu-id="80a2d-136">Określa adresy URL, do których są wysyłane tokeny użytkownika w celu zalogowania się, lub identyfikatory URI przekierowywania, do których są wysyłane kody autoryzacji i tokeny dostępu protokołu OAuth 2.0.</span><span class="sxs-lookup"><span data-stu-id="80a2d-136">Specifies the URLs that user tokens are sent to for sign in, or the redirect URIs that OAuth 2.0 authorization codes and access tokens are sent to.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet, ApplicationIdWithUpdateParamsParameterSet
Aliases: ReplyUrls

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: InputObjectWithUpdateParamsParameterSet
Aliases: ReplyUrls

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80a2d-137">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="80a2d-137">-Confirm</span></span>
<span data-ttu-id="80a2d-138">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="80a2d-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80a2d-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80a2d-139">-WhatIf</span></span>
<span data-ttu-id="80a2d-140">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80a2d-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80a2d-141">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="80a2d-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80a2d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80a2d-142">CommonParameters</span></span>
<span data-ttu-id="80a2d-143">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80a2d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80a2d-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="80a2d-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80a2d-145">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="80a2d-145">INPUTS</span></span>

### <span data-ttu-id="80a2d-146">System.String</span><span class="sxs-lookup"><span data-stu-id="80a2d-146">System.String</span></span>

### <span data-ttu-id="80a2d-147">System.Guid</span><span class="sxs-lookup"><span data-stu-id="80a2d-147">System.Guid</span></span>

### <span data-ttu-id="80a2d-148">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="80a2d-148">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

### <span data-ttu-id="80a2d-149">System.String[]</span><span class="sxs-lookup"><span data-stu-id="80a2d-149">System.String[]</span></span>

### <span data-ttu-id="80a2d-150">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="80a2d-150">System.Boolean</span></span>

## <span data-ttu-id="80a2d-151">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="80a2d-151">OUTPUTS</span></span>

### <span data-ttu-id="80a2d-152">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="80a2d-152">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="80a2d-153">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="80a2d-153">NOTES</span></span>

## <span data-ttu-id="80a2d-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="80a2d-154">RELATED LINKS</span></span>
