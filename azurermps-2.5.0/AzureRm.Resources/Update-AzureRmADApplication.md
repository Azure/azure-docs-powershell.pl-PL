---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/update-azurermadapplication
schema: 2.0.0
ms.openlocfilehash: bf9f993724de9ed20587a3f4ca136c3531689401
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898174"
---
# <span data-ttu-id="7b21a-101">Update-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="7b21a-101">Update-AzureRmADApplication</span></span>

## <span data-ttu-id="7b21a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7b21a-102">SYNOPSIS</span></span>
<span data-ttu-id="7b21a-103">Umożliwia zaktualizowanie istniejącej aplikacji usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7b21a-103">Updates an existing azure active directory application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b21a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7b21a-104">SYNTAX</span></span>

### <span data-ttu-id="7b21a-105">ApplicationObjectIdWithUpdateParamsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7b21a-105">ApplicationObjectIdWithUpdateParamsParameterSet (Default)</span></span>
```
Update-AzureRmADApplication -ObjectId <Guid> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUri <String[]>] [-ReplyUrl <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b21a-106">ApplicationIdWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b21a-106">ApplicationIdWithUpdateParamsParameterSet</span></span>
```
Update-AzureRmADApplication -ApplicationId <Guid> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUri <String[]>] [-ReplyUrl <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b21a-107">InputObjectWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b21a-107">InputObjectWithUpdateParamsParameterSet</span></span>
```
Update-AzureRmADApplication -InputObject <PSADApplication> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUri <String[]>] [-ReplyUrl <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b21a-108">Opis</span><span class="sxs-lookup"><span data-stu-id="7b21a-108">DESCRIPTION</span></span>
<span data-ttu-id="7b21a-109">Umożliwia zaktualizowanie istniejącej aplikacji usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7b21a-109">Updates an existing azure active directory application.</span></span>
<span data-ttu-id="7b21a-110">Aby zaktualizować poświadczenia skojarzone z tą aplikacją, użyj polecenia cmdlet New-AzureRmADAppCredential.</span><span class="sxs-lookup"><span data-stu-id="7b21a-110">To update the credentials associated with this application, please use the New-AzureRmADAppCredential cmdlet.</span></span>

## <span data-ttu-id="7b21a-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7b21a-111">EXAMPLES</span></span>

### <span data-ttu-id="7b21a-112">Przykład 1 — Aktualizowanie nazwy wyświetlanej aplikacji</span><span class="sxs-lookup"><span data-stu-id="7b21a-112">Example 1 - Update the display name of an application</span></span>

```
PS C:\> Update-AzureRmADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName MyNewDisplayName
```

<span data-ttu-id="7b21a-113">Aktualizuje nazwę wyświetlaną aplikacji o identyfikatorze obiektu "fb7b3405-CA44-4b5b-8584-12392f5d96d7" na "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="7b21a-113">Updates the display name of the application with object id 'fb7b3405-ca44-4b5b-8584-12392f5d96d7' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="7b21a-114">Przykład 2 — aktualizowanie wszystkich właściwości aplikacji</span><span class="sxs-lookup"><span data-stu-id="7b21a-114">Example 2 - Update all properties of an application</span></span>

```
PS C:\> Update-AzureRmADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName MyNewDisplayName -HomePage https://www.microsoft.com -IdentifierUris "https://UpdateAppUri"
```

<span data-ttu-id="7b21a-115">Aktualizuje właściwości aplikacji z identyfikatorem obiektu "fb7b3405-CA44-4b5b-8584-12392f5d96d7".</span><span class="sxs-lookup"><span data-stu-id="7b21a-115">Updates the properties of an application with object id 'fb7b3405-ca44-4b5b-8584-12392f5d96d7'.</span></span>

### <span data-ttu-id="7b21a-116">Przykład 3 — Aktualizowanie nazwy wyświetlanej aplikacji przy użyciu połączeń rurowych</span><span class="sxs-lookup"><span data-stu-id="7b21a-116">Example 3 - Update the display name of an application using piping</span></span>

```
PS C:\> Get-AzureRmADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 | Update-AzureRmADApplication -DisplayName MyNewDisplayName
```

<span data-ttu-id="7b21a-117">Pobiera aplikację o identyfikatorze obiektu "fb7b3405-CA44-4b5b-8584-12392f5d96d7" i potokach, które są wyświetlane za pomocą polecenia cmdlet Update-AzureRmADApplication, w celu zaktualizowania nazwy wyświetlanej aplikacji na "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="7b21a-117">Gets the application with object id 'fb7b3405-ca44-4b5b-8584-12392f5d96d7' and pipes that to the Update-AzureRmADApplication cmdlet to update the display name of the application to "MyNewDisplayName".</span></span>

## <span data-ttu-id="7b21a-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7b21a-118">PARAMETERS</span></span>

### <span data-ttu-id="7b21a-119">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="7b21a-119">-ApplicationId</span></span>
<span data-ttu-id="7b21a-120">Identyfikator aplikacji do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="7b21a-120">The application id of the application to update.</span></span>

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

### <span data-ttu-id="7b21a-121">-AvailableToOtherTenants</span><span class="sxs-lookup"><span data-stu-id="7b21a-121">-AvailableToOtherTenants</span></span>
<span data-ttu-id="7b21a-122">Prawda, jeśli aplikacja jest udostępniana innym dzierżawcom; w przeciwnym razie zwraca wartość false.</span><span class="sxs-lookup"><span data-stu-id="7b21a-122">True if the application is shared with other tenants; otherwise, false.</span></span>

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

### <span data-ttu-id="7b21a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b21a-123">-DefaultProfile</span></span>
<span data-ttu-id="7b21a-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7b21a-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b21a-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="7b21a-125">-DisplayName</span></span>
<span data-ttu-id="7b21a-126">Nazwa wyświetlana aplikacji do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="7b21a-126">The display name for the application to update.</span></span>

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

### <span data-ttu-id="7b21a-127">-Strona główna</span><span class="sxs-lookup"><span data-stu-id="7b21a-127">-HomePage</span></span>
<span data-ttu-id="7b21a-128">Adres URL strony głównej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="7b21a-128">The URL to the application's homepage.</span></span>

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

### <span data-ttu-id="7b21a-129">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="7b21a-129">-IdentifierUri</span></span>
<span data-ttu-id="7b21a-130">Identyfikatory URI identyfikujące aplikację.</span><span class="sxs-lookup"><span data-stu-id="7b21a-130">The URIs that identify the application.</span></span>

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

### <span data-ttu-id="7b21a-131">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7b21a-131">-InputObject</span></span>
<span data-ttu-id="7b21a-132">Obiekt reprezentujący aplikację do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="7b21a-132">The object representing the application to update.</span></span>

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

### <span data-ttu-id="7b21a-133">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="7b21a-133">-ObjectId</span></span>
<span data-ttu-id="7b21a-134">Identyfikator obiektu aplikacji do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="7b21a-134">The object id of the application to update.</span></span>

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

### <span data-ttu-id="7b21a-135">-ReplyUrl</span><span class="sxs-lookup"><span data-stu-id="7b21a-135">-ReplyUrl</span></span>
<span data-ttu-id="7b21a-136">Określa adresy URL, do których są wysyłane tokeny użytkowników w celu zalogowania się lub identyfikatory URI przekierowania, do których są wysyłane kody autoryzacji uwierzytelniania OAuth 2,0 oraz tokeny dostępu.</span><span class="sxs-lookup"><span data-stu-id="7b21a-136">Specifies the URLs that user tokens are sent to for sign in, or the redirect URIs that OAuth 2.0 authorization codes and access tokens are sent to.</span></span>

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

### <span data-ttu-id="7b21a-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7b21a-137">-Confirm</span></span>
<span data-ttu-id="7b21a-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b21a-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b21a-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b21a-139">-WhatIf</span></span>
<span data-ttu-id="7b21a-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b21a-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b21a-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7b21a-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b21a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b21a-142">CommonParameters</span></span>
<span data-ttu-id="7b21a-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b21a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b21a-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b21a-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b21a-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7b21a-145">INPUTS</span></span>

### <span data-ttu-id="7b21a-146">System. GUID</span><span class="sxs-lookup"><span data-stu-id="7b21a-146">System.Guid</span></span>

### <span data-ttu-id="7b21a-147">Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="7b21a-147">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="7b21a-148">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7b21a-148">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="7b21a-149">System. String</span><span class="sxs-lookup"><span data-stu-id="7b21a-149">System.String</span></span>

### <span data-ttu-id="7b21a-150">System. String []</span><span class="sxs-lookup"><span data-stu-id="7b21a-150">System.String[]</span></span>

### <span data-ttu-id="7b21a-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7b21a-151">System.Boolean</span></span>

## <span data-ttu-id="7b21a-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7b21a-152">OUTPUTS</span></span>

### <span data-ttu-id="7b21a-153">Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="7b21a-153">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="7b21a-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7b21a-154">NOTES</span></span>

## <span data-ttu-id="7b21a-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7b21a-155">RELATED LINKS</span></span>
