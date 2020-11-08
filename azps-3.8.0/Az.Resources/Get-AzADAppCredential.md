---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6AC9DA05-756D-4D59-BD97-DBAAFBB3C7AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADAppCredential.md
ms.openlocfilehash: ef03850e2a8c0981ad4a1b642df51c1fec462513
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050995"
---
# <span data-ttu-id="cc166-101">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="cc166-101">Get-AzADAppCredential</span></span>

## <span data-ttu-id="cc166-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cc166-102">SYNOPSIS</span></span>
<span data-ttu-id="cc166-103">Pobiera listę poświadczeń skojarzonych z aplikacją.</span><span class="sxs-lookup"><span data-stu-id="cc166-103">Retrieves a list of credentials associated with an application.</span></span>

## <span data-ttu-id="cc166-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cc166-104">SYNTAX</span></span>

### <span data-ttu-id="cc166-105">ApplicationObjectIdParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="cc166-105">ApplicationObjectIdParameterSet (Default)</span></span>
```
Get-AzADAppCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cc166-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc166-106">ApplicationIdParameterSet</span></span>
```
Get-AzADAppCredential -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cc166-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc166-107">DisplayNameParameterSet</span></span>
```
Get-AzADAppCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cc166-108">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc166-108">ApplicationObjectParameterSet</span></span>
```
Get-AzADAppCredential -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cc166-109">Opis</span><span class="sxs-lookup"><span data-stu-id="cc166-109">DESCRIPTION</span></span>
<span data-ttu-id="cc166-110">Polecenie cmdlet Get-AzADAppCredential może służyć do pobierania listy poświadczeń skojarzonych z aplikacją.</span><span class="sxs-lookup"><span data-stu-id="cc166-110">The Get-AzADAppCredential cmdlet can be used to retrieve a list of credentials associated with an application.</span></span>
<span data-ttu-id="cc166-111">To polecenie spowoduje pobranie wszystkich właściwości poświadczeń (ale nie wartości poświadczeń) skojarzonych z aplikacją.</span><span class="sxs-lookup"><span data-stu-id="cc166-111">This command will retrieve all of the credential properties (but not the credential value) associated with the application.</span></span>

## <span data-ttu-id="cc166-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cc166-112">EXAMPLES</span></span>

### <span data-ttu-id="cc166-113">Przykład 1-Uzyskaj poświadczenia aplikacji według identyfikatora obiektu</span><span class="sxs-lookup"><span data-stu-id="cc166-113">Example 1 - Get application credentials by object id</span></span>

```
PS C:\> Get-AzADAppCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
```

<span data-ttu-id="cc166-114">Zwraca listę poświadczeń skojarzonych z aplikacją o identyfikatorze obiektu "1f99cf81-0146-4f4e-beae-2007d0668476".</span><span class="sxs-lookup"><span data-stu-id="cc166-114">Returns a list of credentials associated with the application having object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

### <span data-ttu-id="cc166-115">Przykład 2 — Uzyskaj poświadczenia aplikacji według połączeń rurowych</span><span class="sxs-lookup"><span data-stu-id="cc166-115">Example 2 - Get application credentials by piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 | Get-AzADAppCredential
```

<span data-ttu-id="cc166-116">Pobiera aplikację o identyfikatorze obiektu "1f99cf81-0146-4f4e-beae-2007d0668476" i przekazuje ją do polecenia cmdlet Get-AzADAppCredential, aby wyświetlić wszystkie poświadczenia dla tej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="cc166-116">Gets the application with object id '1f99cf81-0146-4f4e-beae-2007d0668476' and pipes it to the Get-AzADAppCredential cmdlet to list all of the credentials for that application.</span></span>

## <span data-ttu-id="cc166-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cc166-117">PARAMETERS</span></span>

### <span data-ttu-id="cc166-118">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="cc166-118">-ApplicationId</span></span>
<span data-ttu-id="cc166-119">Identyfikator aplikacji, z której mają być pobierane poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="cc166-119">The id of the application to retrieve credentials from.</span></span>

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

### <span data-ttu-id="cc166-120">-Applicationobject</span><span class="sxs-lookup"><span data-stu-id="cc166-120">-ApplicationObject</span></span>
<span data-ttu-id="cc166-121">Obiekt aplikacji, z którego mają zostać pobrane poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="cc166-121">The application object to retrieve credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cc166-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc166-122">-DefaultProfile</span></span>
<span data-ttu-id="cc166-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="cc166-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cc166-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="cc166-124">-DisplayName</span></span>
<span data-ttu-id="cc166-125">Nazwa wyświetlana aplikacji.</span><span class="sxs-lookup"><span data-stu-id="cc166-125">The display name of the application.</span></span>

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

### <span data-ttu-id="cc166-126">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="cc166-126">-ObjectId</span></span>
<span data-ttu-id="cc166-127">Identyfikator obiektu aplikacji, z której mają być pobierane poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="cc166-127">The object id of the application to retrieve credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc166-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc166-128">CommonParameters</span></span>
<span data-ttu-id="cc166-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc166-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc166-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cc166-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc166-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cc166-131">INPUTS</span></span>

### <span data-ttu-id="cc166-132">System. String</span><span class="sxs-lookup"><span data-stu-id="cc166-132">System.String</span></span>

### <span data-ttu-id="cc166-133">System. GUID</span><span class="sxs-lookup"><span data-stu-id="cc166-133">System.Guid</span></span>

### <span data-ttu-id="cc166-134">Microsoft. Azure. Commands. pozycji. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="cc166-134">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="cc166-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cc166-135">OUTPUTS</span></span>

### <span data-ttu-id="cc166-136">Microsoft. Azure. Commands. pozycji. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="cc166-136">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="cc166-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cc166-137">NOTES</span></span>

## <span data-ttu-id="cc166-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cc166-138">RELATED LINKS</span></span>

[<span data-ttu-id="cc166-139">Nowe — AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="cc166-139">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="cc166-140">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="cc166-140">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

[<span data-ttu-id="cc166-141">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="cc166-141">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

