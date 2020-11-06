---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6AC9DA05-756D-4D59-BD97-DBAAFBB3C7AC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADAppCredential.md
ms.openlocfilehash: ba169c54d2b4664473a0013be52e2d078827dcb0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544883"
---
# <span data-ttu-id="3f66b-101">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="3f66b-101">Get-AzureRmADAppCredential</span></span>

## <span data-ttu-id="3f66b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3f66b-102">SYNOPSIS</span></span>
<span data-ttu-id="3f66b-103">Pobiera listę poświadczeń skojarzonych z aplikacją.</span><span class="sxs-lookup"><span data-stu-id="3f66b-103">Retrieves a list of credentials associated with an application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f66b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3f66b-104">SYNTAX</span></span>

### <span data-ttu-id="3f66b-105">ApplicationObjectIdParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3f66b-105">ApplicationObjectIdParameterSet (Default)</span></span>
```
Get-AzureRmADAppCredential -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3f66b-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f66b-106">ApplicationIdParameterSet</span></span>
```
Get-AzureRmADAppCredential -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3f66b-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f66b-107">DisplayNameParameterSet</span></span>
```
Get-AzureRmADAppCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3f66b-108">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f66b-108">ApplicationObjectParameterSet</span></span>
```
Get-AzureRmADAppCredential -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3f66b-109">Opis</span><span class="sxs-lookup"><span data-stu-id="3f66b-109">DESCRIPTION</span></span>
<span data-ttu-id="3f66b-110">Polecenie cmdlet Get-AzureRmADAppCredential może służyć do pobierania listy poświadczeń skojarzonych z aplikacją.</span><span class="sxs-lookup"><span data-stu-id="3f66b-110">The Get-AzureRmADAppCredential cmdlet can be used to retrieve a list of credentials associated with an application.</span></span>
<span data-ttu-id="3f66b-111">To polecenie spowoduje pobranie wszystkich właściwości poświadczeń (ale nie wartości poświadczeń) skojarzonych z aplikacją.</span><span class="sxs-lookup"><span data-stu-id="3f66b-111">This command will retrieve all of the credential properties (but not the credential value) associated with the application.</span></span>

## <span data-ttu-id="3f66b-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3f66b-112">EXAMPLES</span></span>

### <span data-ttu-id="3f66b-113">Przykład 1-Uzyskaj poświadczenia aplikacji według identyfikatora obiektu</span><span class="sxs-lookup"><span data-stu-id="3f66b-113">Example 1 - Get application credentials by object id</span></span>

```
PS C:\> Get-AzureRmADAppCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
```

<span data-ttu-id="3f66b-114">Zwraca listę poświadczeń skojarzonych z aplikacją o identyfikatorze obiektu "1f99cf81-0146-4f4e-beae-2007d0668476".</span><span class="sxs-lookup"><span data-stu-id="3f66b-114">Returns a list of credentials associated with the application having object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

### <span data-ttu-id="3f66b-115">Przykład 2 — Uzyskaj poświadczenia aplikacji według połączeń rurowych</span><span class="sxs-lookup"><span data-stu-id="3f66b-115">Example 2 - Get application credentials by piping</span></span>

```
PS C:\> Get-AzureRmADApplication -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 | Get-AzureRmADAppCredential
```

<span data-ttu-id="3f66b-116">Pobiera aplikację o identyfikatorze obiektu "1f99cf81-0146-4f4e-beae-2007d0668476" i przekazuje ją do polecenia cmdlet Get-AzureRmADAppCredential, aby wyświetlić wszystkie poświadczenia dla tej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="3f66b-116">Gets the application with object id '1f99cf81-0146-4f4e-beae-2007d0668476' and pipes it to the Get-AzureRmADAppCredential cmdlet to list all of the credentials for that application.</span></span>

## <span data-ttu-id="3f66b-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3f66b-117">PARAMETERS</span></span>

### <span data-ttu-id="3f66b-118">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="3f66b-118">-ApplicationId</span></span>
<span data-ttu-id="3f66b-119">Identyfikator aplikacji, z której mają być pobierane poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="3f66b-119">The id of the application to retrieve credentials from.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f66b-120">-Applicationobject</span><span class="sxs-lookup"><span data-stu-id="3f66b-120">-ApplicationObject</span></span>
<span data-ttu-id="3f66b-121">Obiekt aplikacji, z którego mają zostać pobrane poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="3f66b-121">The application object to retrieve credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3f66b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f66b-122">-DefaultProfile</span></span>
<span data-ttu-id="3f66b-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="3f66b-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3f66b-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="3f66b-124">-DisplayName</span></span>
<span data-ttu-id="3f66b-125">Nazwa wyświetlana aplikacji.</span><span class="sxs-lookup"><span data-stu-id="3f66b-125">The display name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f66b-126">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="3f66b-126">-ObjectId</span></span>
<span data-ttu-id="3f66b-127">Identyfikator obiektu aplikacji, z której mają być pobierane poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="3f66b-127">The object id of the application to retrieve credentials from.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f66b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f66b-128">CommonParameters</span></span>
<span data-ttu-id="3f66b-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f66b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f66b-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f66b-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f66b-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3f66b-131">INPUTS</span></span>

### <span data-ttu-id="3f66b-132">System. GUID</span><span class="sxs-lookup"><span data-stu-id="3f66b-132">System.Guid</span></span>

### <span data-ttu-id="3f66b-133">System. String</span><span class="sxs-lookup"><span data-stu-id="3f66b-133">System.String</span></span>

### <span data-ttu-id="3f66b-134">Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="3f66b-134">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="3f66b-135">Parametry: Applicationobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3f66b-135">Parameters: ApplicationObject (ByValue)</span></span>

## <span data-ttu-id="3f66b-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3f66b-136">OUTPUTS</span></span>

### <span data-ttu-id="3f66b-137">Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="3f66b-137">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="3f66b-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3f66b-138">NOTES</span></span>

## <span data-ttu-id="3f66b-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3f66b-139">RELATED LINKS</span></span>

[<span data-ttu-id="3f66b-140">Nowe — AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="3f66b-140">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="3f66b-141">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="3f66b-141">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

[<span data-ttu-id="3f66b-142">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="3f66b-142">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

