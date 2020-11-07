---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6AC9DA05-756D-4D59-BD97-DBAAFBB3C7AC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadappcredential
schema: 2.0.0
ms.openlocfilehash: 5390cf033174f473a08a8407028a709a02677352
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898213"
---
# <span data-ttu-id="dc587-101">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="dc587-101">Get-AzureRmADAppCredential</span></span>

## <span data-ttu-id="dc587-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dc587-102">SYNOPSIS</span></span>
<span data-ttu-id="dc587-103">Pobiera listę poświadczeń skojarzonych z aplikacją.</span><span class="sxs-lookup"><span data-stu-id="dc587-103">Retrieves a list of credentials associated with an application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc587-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dc587-104">SYNTAX</span></span>

### <span data-ttu-id="dc587-105">ApplicationObjectIdParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="dc587-105">ApplicationObjectIdParameterSet (Default)</span></span>
```
Get-AzureRmADAppCredential -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc587-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc587-106">ApplicationIdParameterSet</span></span>
```
Get-AzureRmADAppCredential -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dc587-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc587-107">DisplayNameParameterSet</span></span>
```
Get-AzureRmADAppCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dc587-108">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc587-108">ApplicationObjectParameterSet</span></span>
```
Get-AzureRmADAppCredential -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dc587-109">Opis</span><span class="sxs-lookup"><span data-stu-id="dc587-109">DESCRIPTION</span></span>
<span data-ttu-id="dc587-110">Polecenie cmdlet Get-AzureRmADAppCredential może służyć do pobierania listy poświadczeń skojarzonych z aplikacją.</span><span class="sxs-lookup"><span data-stu-id="dc587-110">The Get-AzureRmADAppCredential cmdlet can be used to retrieve a list of credentials associated with an application.</span></span>
<span data-ttu-id="dc587-111">To polecenie spowoduje pobranie wszystkich właściwości poświadczeń (ale nie wartości poświadczeń) skojarzonych z aplikacją.</span><span class="sxs-lookup"><span data-stu-id="dc587-111">This command will retrieve all of the credential properties (but not the credential value) associated with the application.</span></span>

## <span data-ttu-id="dc587-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dc587-112">EXAMPLES</span></span>

### <span data-ttu-id="dc587-113">Przykład 1-Uzyskaj poświadczenia aplikacji według identyfikatora obiektu</span><span class="sxs-lookup"><span data-stu-id="dc587-113">Example 1 - Get application credentials by object id</span></span>

```
PS C:\> Get-AzureRmADAppCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
```

<span data-ttu-id="dc587-114">Zwraca listę poświadczeń skojarzonych z aplikacją o identyfikatorze obiektu "1f99cf81-0146-4f4e-beae-2007d0668476".</span><span class="sxs-lookup"><span data-stu-id="dc587-114">Returns a list of credentials associated with the application having object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

### <span data-ttu-id="dc587-115">Przykład 2 — Uzyskaj poświadczenia aplikacji według połączeń rurowych</span><span class="sxs-lookup"><span data-stu-id="dc587-115">Example 2 - Get application credentials by piping</span></span>

```
PS C:\> Get-AzureRmADApplication -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 | Get-AzureRmADAppCredential
```

<span data-ttu-id="dc587-116">Pobiera aplikację o identyfikatorze obiektu "1f99cf81-0146-4f4e-beae-2007d0668476" i przekazuje ją do polecenia cmdlet Get-AzureRmADAppCredential, aby wyświetlić wszystkie poświadczenia dla tej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="dc587-116">Gets the application with object id '1f99cf81-0146-4f4e-beae-2007d0668476' and pipes it to the Get-AzureRmADAppCredential cmdlet to list all of the credentials for that application.</span></span>

## <span data-ttu-id="dc587-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dc587-117">PARAMETERS</span></span>

### <span data-ttu-id="dc587-118">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="dc587-118">-ApplicationId</span></span>
<span data-ttu-id="dc587-119">Identyfikator aplikacji, z której mają być pobierane poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="dc587-119">The id of the application to retrieve credentials from.</span></span>

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

### <span data-ttu-id="dc587-120">-Applicationobject</span><span class="sxs-lookup"><span data-stu-id="dc587-120">-ApplicationObject</span></span>
<span data-ttu-id="dc587-121">Obiekt aplikacji, z którego mają zostać pobrane poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="dc587-121">The application object to retrieve credentials from.</span></span>

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

### <span data-ttu-id="dc587-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc587-122">-DefaultProfile</span></span>
<span data-ttu-id="dc587-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="dc587-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dc587-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="dc587-124">-DisplayName</span></span>
<span data-ttu-id="dc587-125">Nazwa wyświetlana aplikacji.</span><span class="sxs-lookup"><span data-stu-id="dc587-125">The display name of the application.</span></span>

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

### <span data-ttu-id="dc587-126">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="dc587-126">-ObjectId</span></span>
<span data-ttu-id="dc587-127">Identyfikator obiektu aplikacji, z której mają być pobierane poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="dc587-127">The object id of the application to retrieve credentials from.</span></span>

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

### <span data-ttu-id="dc587-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc587-128">CommonParameters</span></span>
<span data-ttu-id="dc587-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc587-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc587-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc587-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc587-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dc587-131">INPUTS</span></span>

### <span data-ttu-id="dc587-132">System. GUID</span><span class="sxs-lookup"><span data-stu-id="dc587-132">System.Guid</span></span>

### <span data-ttu-id="dc587-133">System. String</span><span class="sxs-lookup"><span data-stu-id="dc587-133">System.String</span></span>

### <span data-ttu-id="dc587-134">Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="dc587-134">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="dc587-135">Parametry: Applicationobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="dc587-135">Parameters: ApplicationObject (ByValue)</span></span>

## <span data-ttu-id="dc587-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dc587-136">OUTPUTS</span></span>

### <span data-ttu-id="dc587-137">Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="dc587-137">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="dc587-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dc587-138">NOTES</span></span>

## <span data-ttu-id="dc587-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dc587-139">RELATED LINKS</span></span>

[<span data-ttu-id="dc587-140">Nowe — AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="dc587-140">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="dc587-141">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="dc587-141">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

[<span data-ttu-id="dc587-142">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="dc587-142">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

