---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-Azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Update-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Update-AzADApplication.md
ms.openlocfilehash: 8eb01ccfa16b1d3610468f98117ee650376d4b6c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892309"
---
# <span data-ttu-id="3e953-101">Update-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="3e953-101">Update-AzADApplication</span></span>

## <span data-ttu-id="3e953-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3e953-102">SYNOPSIS</span></span>
<span data-ttu-id="3e953-103">Umożliwia zaktualizowanie istniejącej aplikacji usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="3e953-103">Updates an existing azure active directory application.</span></span>

## <span data-ttu-id="3e953-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3e953-104">SYNTAX</span></span>

### <span data-ttu-id="3e953-105">ApplicationObjectIdWithUpdateParamsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3e953-105">ApplicationObjectIdWithUpdateParamsParameterSet (Default)</span></span>
```
Update-AzADApplication -ObjectId <Guid> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUri <String[]>] [-ReplyUrl <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e953-106">ApplicationIdWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e953-106">ApplicationIdWithUpdateParamsParameterSet</span></span>
```
Update-AzADApplication -ApplicationId <Guid> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUri <String[]>] [-ReplyUrl <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e953-107">InputObjectWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e953-107">InputObjectWithUpdateParamsParameterSet</span></span>
```
Update-AzADApplication -InputObject <PSADApplication> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUri <String[]>] [-ReplyUrl <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e953-108">Opis</span><span class="sxs-lookup"><span data-stu-id="3e953-108">DESCRIPTION</span></span>
<span data-ttu-id="3e953-109">Umożliwia zaktualizowanie istniejącej aplikacji usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="3e953-109">Updates an existing azure active directory application.</span></span>
<span data-ttu-id="3e953-110">Aby zaktualizować poświadczenia skojarzone z tą aplikacją, użyj polecenia cmdlet New-AzADAppCredential.</span><span class="sxs-lookup"><span data-stu-id="3e953-110">To update the credentials associated with this application, please use the New-AzADAppCredential cmdlet.</span></span>

## <span data-ttu-id="3e953-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3e953-111">EXAMPLES</span></span>

### <span data-ttu-id="3e953-112">Przykład 1 — Aktualizowanie nazwy wyświetlanej aplikacji</span><span class="sxs-lookup"><span data-stu-id="3e953-112">Example 1 - Update the display name of an application</span></span>

```
PS C:\> Update-AzADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName MyNewDisplayName
```

<span data-ttu-id="3e953-113">Aktualizuje nazwę wyświetlaną aplikacji o identyfikatorze obiektu "fb7b3405-CA44-4b5b-8584-12392f5d96d7" na "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="3e953-113">Updates the display name of the application with object id 'fb7b3405-ca44-4b5b-8584-12392f5d96d7' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="3e953-114">Przykład 2 — aktualizowanie wszystkich właściwości aplikacji</span><span class="sxs-lookup"><span data-stu-id="3e953-114">Example 2 - Update all properties of an application</span></span>

```
PS C:\> Update-AzADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName MyNewDisplayName -HomePage https://www.microsoft.com -IdentifierUris "https://UpdateAppUri"
```

<span data-ttu-id="3e953-115">Aktualizuje właściwości aplikacji z identyfikatorem obiektu "fb7b3405-CA44-4b5b-8584-12392f5d96d7".</span><span class="sxs-lookup"><span data-stu-id="3e953-115">Updates the properties of an application with object id 'fb7b3405-ca44-4b5b-8584-12392f5d96d7'.</span></span>

### <span data-ttu-id="3e953-116">Przykład 3 — Aktualizowanie nazwy wyświetlanej aplikacji przy użyciu połączeń rurowych</span><span class="sxs-lookup"><span data-stu-id="3e953-116">Example 3 - Update the display name of an application using piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 | Update-AzADApplication -DisplayName MyNewDisplayName
```

<span data-ttu-id="3e953-117">Pobiera aplikację o identyfikatorze obiektu "fb7b3405-CA44-4b5b-8584-12392f5d96d7" i potokach, które są wyświetlane za pomocą polecenia cmdlet Update-AzADApplication, w celu zaktualizowania nazwy wyświetlanej aplikacji na "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="3e953-117">Gets the application with object id 'fb7b3405-ca44-4b5b-8584-12392f5d96d7' and pipes that to the Update-AzADApplication cmdlet to update the display name of the application to "MyNewDisplayName".</span></span>

## <span data-ttu-id="3e953-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3e953-118">PARAMETERS</span></span>

### <span data-ttu-id="3e953-119">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="3e953-119">-ApplicationId</span></span>
<span data-ttu-id="3e953-120">Identyfikator aplikacji do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="3e953-120">The application id of the application to update.</span></span>

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

### <span data-ttu-id="3e953-121">-AvailableToOtherTenants</span><span class="sxs-lookup"><span data-stu-id="3e953-121">-AvailableToOtherTenants</span></span>
<span data-ttu-id="3e953-122">Prawda, jeśli aplikacja jest udostępniana innym dzierżawcom; w przeciwnym razie zwraca wartość false.</span><span class="sxs-lookup"><span data-stu-id="3e953-122">True if the application is shared with other tenants; otherwise, false.</span></span>

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

### <span data-ttu-id="3e953-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e953-123">-DefaultProfile</span></span>
<span data-ttu-id="3e953-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3e953-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e953-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="3e953-125">-DisplayName</span></span>
<span data-ttu-id="3e953-126">Nazwa wyświetlana aplikacji do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="3e953-126">The display name for the application to update.</span></span>

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

### <span data-ttu-id="3e953-127">-Strona główna</span><span class="sxs-lookup"><span data-stu-id="3e953-127">-HomePage</span></span>
<span data-ttu-id="3e953-128">Adres URL strony głównej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="3e953-128">The URL to the application's homepage.</span></span>

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

### <span data-ttu-id="3e953-129">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="3e953-129">-IdentifierUri</span></span>
<span data-ttu-id="3e953-130">Identyfikatory URI identyfikujące aplikację.</span><span class="sxs-lookup"><span data-stu-id="3e953-130">The URIs that identify the application.</span></span>

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

### <span data-ttu-id="3e953-131">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3e953-131">-InputObject</span></span>
<span data-ttu-id="3e953-132">Obiekt reprezentujący aplikację do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="3e953-132">The object representing the application to update.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: InputObjectWithUpdateParamsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3e953-133">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="3e953-133">-ObjectId</span></span>
<span data-ttu-id="3e953-134">Identyfikator obiektu aplikacji do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="3e953-134">The object id of the application to update.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e953-135">-ReplyUrl</span><span class="sxs-lookup"><span data-stu-id="3e953-135">-ReplyUrl</span></span>
<span data-ttu-id="3e953-136">Określa adresy URL, do których są wysyłane tokeny użytkowników w celu zalogowania się lub identyfikatory URI przekierowania, do których są wysyłane kody autoryzacji uwierzytelniania OAuth 2,0 oraz tokeny dostępu.</span><span class="sxs-lookup"><span data-stu-id="3e953-136">Specifies the URLs that user tokens are sent to for sign in, or the redirect URIs that OAuth 2.0 authorization codes and access tokens are sent to.</span></span>

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

### <span data-ttu-id="3e953-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3e953-137">-Confirm</span></span>
<span data-ttu-id="3e953-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e953-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e953-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e953-139">-WhatIf</span></span>
<span data-ttu-id="3e953-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e953-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e953-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3e953-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e953-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e953-142">CommonParameters</span></span>
<span data-ttu-id="3e953-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e953-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e953-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e953-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e953-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3e953-145">INPUTS</span></span>

### <span data-ttu-id="3e953-146">System. GUID</span><span class="sxs-lookup"><span data-stu-id="3e953-146">System.Guid</span></span>

### <span data-ttu-id="3e953-147">Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="3e953-147">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="3e953-148">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3e953-148">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="3e953-149">System. String</span><span class="sxs-lookup"><span data-stu-id="3e953-149">System.String</span></span>

### <span data-ttu-id="3e953-150">System. String []</span><span class="sxs-lookup"><span data-stu-id="3e953-150">System.String[]</span></span>

### <span data-ttu-id="3e953-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3e953-151">System.Boolean</span></span>

## <span data-ttu-id="3e953-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3e953-152">OUTPUTS</span></span>

### <span data-ttu-id="3e953-153">Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="3e953-153">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="3e953-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3e953-154">NOTES</span></span>

## <span data-ttu-id="3e953-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3e953-155">RELATED LINKS</span></span>
