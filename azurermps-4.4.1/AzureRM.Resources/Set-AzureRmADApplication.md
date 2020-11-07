---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BA97DB6F-F64D-417E-BD72-C2EBB2EC1AA4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADApplication.md
ms.openlocfilehash: 6fbbed83f9565a81b305df5cf8b66fd8210c6aec
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719249"
---
# <span data-ttu-id="ad112-101">Set-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="ad112-101">Set-AzureRmADApplication</span></span>

## <span data-ttu-id="ad112-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ad112-102">SYNOPSIS</span></span>
<span data-ttu-id="ad112-103">Umożliwia zaktualizowanie istniejącej aplikacji usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ad112-103">Updates an existing azure active directory application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad112-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ad112-104">SYNTAX</span></span>

### <span data-ttu-id="ad112-105">ApplicationObjectIdWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad112-105">ApplicationObjectIdWithUpdateParamsParameterSet</span></span>
```
Set-AzureRmADApplication -ObjectId <String> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUris <String[]>] [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad112-106">ApplicationIdWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad112-106">ApplicationIdWithUpdateParamsParameterSet</span></span>
```
Set-AzureRmADApplication -ApplicationId <String> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUris <String[]>] [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad112-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ad112-107">DESCRIPTION</span></span>
<span data-ttu-id="ad112-108">Umożliwia zaktualizowanie istniejącej aplikacji usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ad112-108">Updates an existing azure active directory application.</span></span>
<span data-ttu-id="ad112-109">Aby zaktualizować poświadczenia skojarzone z tą aplikacją, użyj polecenia cmdlet New-AzureRmADAppCredential.</span><span class="sxs-lookup"><span data-stu-id="ad112-109">To update the credentials associated with this application, please use New-AzureRmADAppCredential cmdlet.</span></span>

## <span data-ttu-id="ad112-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ad112-110">EXAMPLES</span></span>

### <span data-ttu-id="ad112-111">--------------------------Przykład 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="ad112-111">--------------------------  Example 1  --------------------------</span></span>
```
PS E:\> Set-AzureRmADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName "UpdatedAppName" -HomePage "https://www.microsoft.com" -IdentifierUris "http://UpdatedApp" -AvailableToOtherTenants $false
```

<span data-ttu-id="ad112-112">Aktualizuje właściwości istniejącej aplikacji usługi Azure Active Directory z identyfikatorem obiektu objectId "fb7b3405-CA44-4b5b-8584-12392f5d96d7".</span><span class="sxs-lookup"><span data-stu-id="ad112-112">Updates the properties of an existing azure active directory application with objectId "fb7b3405-ca44-4b5b-8584-12392f5d96d7".</span></span>

### <span data-ttu-id="ad112-113">--------------------------Przykład 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="ad112-113">--------------------------  Example 2  --------------------------</span></span>
```
PS E:\> Set-AzureRmADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName "UpdatedAppName"
```

<span data-ttu-id="ad112-114">Aktualizuje nazwę wyświetlaną istniejącej aplikacji usługi Azure Active Directory z identyfikatorem obiektu objectId "fb7b3405-CA44-4b5b-8584-12392f5d96d7".</span><span class="sxs-lookup"><span data-stu-id="ad112-114">Updates the display name of an existing azure active directory application with objectId "fb7b3405-ca44-4b5b-8584-12392f5d96d7".</span></span>

## <span data-ttu-id="ad112-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ad112-115">PARAMETERS</span></span>

### <span data-ttu-id="ad112-116">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="ad112-116">-ApplicationId</span></span>
<span data-ttu-id="ad112-117">Identyfikator aplikacji do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="ad112-117">The id of the application to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationIdWithUpdateParamsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad112-118">-AvailableToOtherTenants</span><span class="sxs-lookup"><span data-stu-id="ad112-118">-AvailableToOtherTenants</span></span>
<span data-ttu-id="ad112-119">Wartość określająca, czy aplikacja została zaktualizowana w ramach pojedynczej dzierżawy, czy do wielu dzierżawców.</span><span class="sxs-lookup"><span data-stu-id="ad112-119">The value specifying whether the application is updated to be a single tenant or a multi-tenant.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad112-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ad112-120">-DisplayName</span></span>
<span data-ttu-id="ad112-121">Nowa nazwa wyświetlana aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ad112-121">New Display name for the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad112-122">-Strona główna</span><span class="sxs-lookup"><span data-stu-id="ad112-122">-HomePage</span></span>
<span data-ttu-id="ad112-123">Nowy adres URL strony głównej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ad112-123">New URL of the application homepage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad112-124">-IdentifierUris</span><span class="sxs-lookup"><span data-stu-id="ad112-124">-IdentifierUris</span></span>
<span data-ttu-id="ad112-125">Nowe identyfikatory URI identyfikujące aplikację.</span><span class="sxs-lookup"><span data-stu-id="ad112-125">New URIs that identify the application.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad112-126">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="ad112-126">-ObjectId</span></span>
<span data-ttu-id="ad112-127">Identyfikator obiektu aplikacji do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="ad112-127">The object id of the application to update.</span></span>

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

### <span data-ttu-id="ad112-128">-ReplyUrls</span><span class="sxs-lookup"><span data-stu-id="ad112-128">-ReplyUrls</span></span>
<span data-ttu-id="ad112-129">Nowe adresy URL odpowiedzi dla aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ad112-129">New reply urls for the application.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad112-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ad112-130">-Confirm</span></span>
<span data-ttu-id="ad112-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad112-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad112-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad112-132">-WhatIf</span></span>
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

### <span data-ttu-id="ad112-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad112-133">-DefaultProfile</span></span>
<span data-ttu-id="ad112-134">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ad112-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad112-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad112-135">CommonParameters</span></span>
<span data-ttu-id="ad112-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad112-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad112-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad112-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad112-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ad112-138">INPUTS</span></span>

## <span data-ttu-id="ad112-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ad112-139">OUTPUTS</span></span>

### <span data-ttu-id="ad112-140">Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="ad112-140">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="ad112-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ad112-141">NOTES</span></span>

## <span data-ttu-id="ad112-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ad112-142">RELATED LINKS</span></span>

[<span data-ttu-id="ad112-143">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="ad112-143">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="ad112-144">Nowe — AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="ad112-144">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

[<span data-ttu-id="ad112-145">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="ad112-145">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="ad112-146">Nowe — AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="ad112-146">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="ad112-147">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="ad112-147">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="ad112-148">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="ad112-148">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

