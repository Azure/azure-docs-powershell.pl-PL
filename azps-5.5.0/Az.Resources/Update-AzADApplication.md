---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADApplication.md
ms.openlocfilehash: c4754ecf8cae06fd43f57bc50d3b3fbeaf1d5081
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242435"
---
# <span data-ttu-id="58956-101">Update-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="58956-101">Update-AzADApplication</span></span>

## <span data-ttu-id="58956-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58956-102">SYNOPSIS</span></span>
<span data-ttu-id="58956-103">Aktualizuje istniejącą aplikację usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="58956-103">Updates an existing azure active directory application.</span></span>

## <span data-ttu-id="58956-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="58956-104">SYNTAX</span></span>

### <span data-ttu-id="58956-105">ApplicationObjectIdWithUpdateParamsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="58956-105">ApplicationObjectIdWithUpdateParamsParameterSet (Default)</span></span>
```
Update-AzADApplication -ObjectId <String> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUri <String[]>] [-ReplyUrl <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58956-106">ApplicationIdWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="58956-106">ApplicationIdWithUpdateParamsParameterSet</span></span>
```
Update-AzADApplication -ApplicationId <Guid> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUri <String[]>] [-ReplyUrl <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58956-107">InputObjectWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="58956-107">InputObjectWithUpdateParamsParameterSet</span></span>
```
Update-AzADApplication -InputObject <PSADApplication> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUri <String[]>] [-ReplyUrl <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58956-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="58956-108">DESCRIPTION</span></span>
<span data-ttu-id="58956-109">Aktualizuje istniejącą aplikację usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="58956-109">Updates an existing azure active directory application.</span></span>
<span data-ttu-id="58956-110">Aby zaktualizować poświadczenia skojarzone z tą aplikacją, użyj New-AzADAppCredential cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58956-110">To update the credentials associated with this application, please use the New-AzADAppCredential cmdlet.</span></span>

## <span data-ttu-id="58956-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="58956-111">EXAMPLES</span></span>

### <span data-ttu-id="58956-112">Przykład 1. Aktualizowanie nazwy wyświetlanej aplikacji</span><span class="sxs-lookup"><span data-stu-id="58956-112">Example 1 - Update the display name of an application</span></span>

```
PS C:\> Update-AzADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName MyNewDisplayName
```

<span data-ttu-id="58956-113">Aktualizuje nazwę wyświetlaną aplikacji o identyfikatorze obiektu "fb7b3405-ca44-4b5b-8584-12392f5d96d7" na "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="58956-113">Updates the display name of the application with object id 'fb7b3405-ca44-4b5b-8584-12392f5d96d7' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="58956-114">Przykład 2. Aktualizowanie wszystkich właściwości aplikacji</span><span class="sxs-lookup"><span data-stu-id="58956-114">Example 2 - Update all properties of an application</span></span>

```
PS C:\> Update-AzADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName MyNewDisplayName -HomePage https://www.microsoft.com -IdentifierUris "https://UpdateAppUri"
```

<span data-ttu-id="58956-115">Aktualizuje właściwości aplikacji za pomocą identyfikatora obiektu "fb7b3405-ca44-4b5b-8584-12392f5d96d7".</span><span class="sxs-lookup"><span data-stu-id="58956-115">Updates the properties of an application with object id 'fb7b3405-ca44-4b5b-8584-12392f5d96d7'.</span></span>

### <span data-ttu-id="58956-116">Przykład 3. Aktualizowanie nazwy wyświetlanej aplikacji za pomocą rur</span><span class="sxs-lookup"><span data-stu-id="58956-116">Example 3 - Update the display name of an application using piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 | Update-AzADApplication -DisplayName MyNewDisplayName
```

<span data-ttu-id="58956-117">Pobiera aplikację o identyfikatorze obiektu "fb7b3405-ca44-4b5b-8584-12392f5d96d7" i potoki, które są przekierowywane do polecenia cmdlet programu Update-AzADApplication w celu zaktualizowania nazwy wyświetlanej aplikacji do wartości "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="58956-117">Gets the application with object id 'fb7b3405-ca44-4b5b-8584-12392f5d96d7' and pipes that to the Update-AzADApplication cmdlet to update the display name of the application to "MyNewDisplayName".</span></span>

## <span data-ttu-id="58956-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="58956-118">PARAMETERS</span></span>

### <span data-ttu-id="58956-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="58956-119">-ApplicationId</span></span>
<span data-ttu-id="58956-120">Identyfikator aplikacji do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="58956-120">The application id of the application to update.</span></span>

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

### <span data-ttu-id="58956-121">-AvailableToOtherTenants</span><span class="sxs-lookup"><span data-stu-id="58956-121">-AvailableToOtherTenants</span></span>
<span data-ttu-id="58956-122">Ma wartość True (Prawda), jeśli aplikacja jest udostępniana innym dzierżawom; w przeciwnym razie fałsz.</span><span class="sxs-lookup"><span data-stu-id="58956-122">True if the application is shared with other tenants; otherwise, false.</span></span>

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

### <span data-ttu-id="58956-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58956-123">-DefaultProfile</span></span>
<span data-ttu-id="58956-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="58956-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58956-125">— DisplayName</span><span class="sxs-lookup"><span data-stu-id="58956-125">-DisplayName</span></span>
<span data-ttu-id="58956-126">Nazwa wyświetlana aplikacji do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="58956-126">The display name for the application to update.</span></span>

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

### <span data-ttu-id="58956-127">-Strona główna</span><span class="sxs-lookup"><span data-stu-id="58956-127">-HomePage</span></span>
<span data-ttu-id="58956-128">Adres URL strony głównej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="58956-128">The URL to the application's homepage.</span></span>

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

### <span data-ttu-id="58956-129">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="58956-129">-IdentifierUri</span></span>
<span data-ttu-id="58956-130">URI identyfikujące aplikację.</span><span class="sxs-lookup"><span data-stu-id="58956-130">The URIs that identify the application.</span></span>

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

### <span data-ttu-id="58956-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="58956-131">-InputObject</span></span>
<span data-ttu-id="58956-132">Obiekt reprezentujący aplikację do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="58956-132">The object representing the application to update.</span></span>

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

### <span data-ttu-id="58956-133">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="58956-133">-ObjectId</span></span>
<span data-ttu-id="58956-134">Identyfikator obiektu aplikacji do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="58956-134">The object id of the application to update.</span></span>

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

### <span data-ttu-id="58956-135">- ReplyUrl</span><span class="sxs-lookup"><span data-stu-id="58956-135">-ReplyUrl</span></span>
<span data-ttu-id="58956-136">Określa adresy URL, do których są wysyłane tokeny użytkownika w celu zalogowania się, lub identyfikatory URI przekierowywania, do których są wysyłane kody autoryzacji i tokeny dostępu protokołu OAuth 2.0.</span><span class="sxs-lookup"><span data-stu-id="58956-136">Specifies the URLs that user tokens are sent to for sign in, or the redirect URIs that OAuth 2.0 authorization codes and access tokens are sent to.</span></span>

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

### <span data-ttu-id="58956-137">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="58956-137">-Confirm</span></span>
<span data-ttu-id="58956-138">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="58956-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58956-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58956-139">-WhatIf</span></span>
<span data-ttu-id="58956-140">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58956-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58956-141">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="58956-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58956-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58956-142">CommonParameters</span></span>
<span data-ttu-id="58956-143">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58956-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58956-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="58956-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58956-145">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="58956-145">INPUTS</span></span>

### <span data-ttu-id="58956-146">System.String</span><span class="sxs-lookup"><span data-stu-id="58956-146">System.String</span></span>

### <span data-ttu-id="58956-147">System.Guid</span><span class="sxs-lookup"><span data-stu-id="58956-147">System.Guid</span></span>

### <span data-ttu-id="58956-148">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="58956-148">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

### <span data-ttu-id="58956-149">System.String[]</span><span class="sxs-lookup"><span data-stu-id="58956-149">System.String[]</span></span>

### <span data-ttu-id="58956-150">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="58956-150">System.Boolean</span></span>

## <span data-ttu-id="58956-151">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="58956-151">OUTPUTS</span></span>

### <span data-ttu-id="58956-152">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="58956-152">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="58956-153">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="58956-153">NOTES</span></span>

## <span data-ttu-id="58956-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="58956-154">RELATED LINKS</span></span>
