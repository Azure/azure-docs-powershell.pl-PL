---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BA97DB6F-F64D-417E-BD72-C2EBB2EC1AA4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADApplication.md
ms.openlocfilehash: a8c1aa2d0f22a9c6dc6260384e51140cb930106a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551623"
---
# <span data-ttu-id="69814-101">Set-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="69814-101">Set-AzureRmADApplication</span></span>

## <span data-ttu-id="69814-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="69814-102">SYNOPSIS</span></span>
<span data-ttu-id="69814-103">Umożliwia zaktualizowanie istniejącej aplikacji usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="69814-103">Updates an existing azure active directory application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69814-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="69814-104">SYNTAX</span></span>

### <span data-ttu-id="69814-105">ApplicationObjectIdWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="69814-105">ApplicationObjectIdWithUpdateParamsParameterSet</span></span>
```
Set-AzureRmADApplication -ObjectId <String> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUris <String[]>] [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69814-106">ApplicationIdWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="69814-106">ApplicationIdWithUpdateParamsParameterSet</span></span>
```
Set-AzureRmADApplication -ApplicationId <String> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUris <String[]>] [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69814-107">Opis</span><span class="sxs-lookup"><span data-stu-id="69814-107">DESCRIPTION</span></span>
<span data-ttu-id="69814-108">Umożliwia zaktualizowanie istniejącej aplikacji usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="69814-108">Updates an existing azure active directory application.</span></span>
<span data-ttu-id="69814-109">Aby zaktualizować poświadczenia skojarzone z tą aplikacją, użyj polecenia cmdlet New-AzureRmADAppCredential.</span><span class="sxs-lookup"><span data-stu-id="69814-109">To update the credentials associated with this application, please use New-AzureRmADAppCredential cmdlet.</span></span>

## <span data-ttu-id="69814-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="69814-110">EXAMPLES</span></span>

### <span data-ttu-id="69814-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="69814-111">Example 1</span></span>
```
PS E:\> Set-AzureRmADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName "UpdatedAppName" -HomePage "https://www.microsoft.com" -IdentifierUris "http://UpdatedApp" -AvailableToOtherTenants $false
```

<span data-ttu-id="69814-112">Aktualizuje właściwości istniejącej aplikacji usługi Azure Active Directory z identyfikatorem obiektu objectId "fb7b3405-CA44-4b5b-8584-12392f5d96d7".</span><span class="sxs-lookup"><span data-stu-id="69814-112">Updates the properties of an existing azure active directory application with objectId "fb7b3405-ca44-4b5b-8584-12392f5d96d7".</span></span>

### <span data-ttu-id="69814-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="69814-113">Example 2</span></span>
```
PS E:\> Set-AzureRmADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName "UpdatedAppName"
```

<span data-ttu-id="69814-114">Aktualizuje nazwę wyświetlaną istniejącej aplikacji usługi Azure Active Directory z identyfikatorem obiektu objectId "fb7b3405-CA44-4b5b-8584-12392f5d96d7".</span><span class="sxs-lookup"><span data-stu-id="69814-114">Updates the display name of an existing azure active directory application with objectId "fb7b3405-ca44-4b5b-8584-12392f5d96d7".</span></span>

## <span data-ttu-id="69814-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="69814-115">PARAMETERS</span></span>

### <span data-ttu-id="69814-116">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="69814-116">-ApplicationId</span></span>
<span data-ttu-id="69814-117">Identyfikator aplikacji do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="69814-117">The id of the application to update.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationIdWithUpdateParamsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69814-118">-AvailableToOtherTenants</span><span class="sxs-lookup"><span data-stu-id="69814-118">-AvailableToOtherTenants</span></span>
<span data-ttu-id="69814-119">Wartość określająca, czy aplikacja została zaktualizowana w ramach pojedynczej dzierżawy, czy do wielu dzierżawców.</span><span class="sxs-lookup"><span data-stu-id="69814-119">The value specifying whether the application is updated to be a single tenant or a multi-tenant.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69814-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69814-120">-DefaultProfile</span></span>
<span data-ttu-id="69814-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="69814-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69814-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="69814-122">-DisplayName</span></span>
<span data-ttu-id="69814-123">Nowa nazwa wyświetlana aplikacji.</span><span class="sxs-lookup"><span data-stu-id="69814-123">New Display name for the application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69814-124">-Strona główna</span><span class="sxs-lookup"><span data-stu-id="69814-124">-HomePage</span></span>
<span data-ttu-id="69814-125">Nowy adres URL strony głównej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="69814-125">New URL of the application homepage.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69814-126">-IdentifierUris</span><span class="sxs-lookup"><span data-stu-id="69814-126">-IdentifierUris</span></span>
<span data-ttu-id="69814-127">Nowe identyfikatory URI identyfikujące aplikację.</span><span class="sxs-lookup"><span data-stu-id="69814-127">New URIs that identify the application.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69814-128">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="69814-128">-ObjectId</span></span>
<span data-ttu-id="69814-129">Identyfikator obiektu aplikacji do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="69814-129">The object id of the application to update.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69814-130">-ReplyUrls</span><span class="sxs-lookup"><span data-stu-id="69814-130">-ReplyUrls</span></span>
<span data-ttu-id="69814-131">Nowe adresy URL odpowiedzi dla aplikacji.</span><span class="sxs-lookup"><span data-stu-id="69814-131">New reply urls for the application.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69814-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="69814-132">-Confirm</span></span>
<span data-ttu-id="69814-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69814-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69814-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69814-134">-WhatIf</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69814-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69814-135">CommonParameters</span></span>
<span data-ttu-id="69814-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69814-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69814-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69814-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69814-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="69814-138">INPUTS</span></span>

### <span data-ttu-id="69814-139">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="69814-139">None</span></span>
<span data-ttu-id="69814-140">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="69814-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="69814-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="69814-141">OUTPUTS</span></span>

### <span data-ttu-id="69814-142">Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="69814-142">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="69814-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="69814-143">NOTES</span></span>

## <span data-ttu-id="69814-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="69814-144">RELATED LINKS</span></span>

[<span data-ttu-id="69814-145">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="69814-145">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="69814-146">Nowe — AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="69814-146">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

[<span data-ttu-id="69814-147">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="69814-147">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="69814-148">Nowe — AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="69814-148">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="69814-149">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="69814-149">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="69814-150">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="69814-150">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

