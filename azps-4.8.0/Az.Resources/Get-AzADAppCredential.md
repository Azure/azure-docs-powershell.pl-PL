---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6AC9DA05-756D-4D59-BD97-DBAAFBB3C7AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADAppCredential.md
ms.openlocfilehash: 7bfa908e83d7731ca2ed5613d82f42b19c392b2f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221141"
---
# <span data-ttu-id="f3361-101">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="f3361-101">Get-AzADAppCredential</span></span>

## <span data-ttu-id="f3361-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f3361-102">SYNOPSIS</span></span>
<span data-ttu-id="f3361-103">Pobiera listę poświadczeń skojarzonych z aplikacją.</span><span class="sxs-lookup"><span data-stu-id="f3361-103">Retrieves a list of credentials associated with an application.</span></span>

## <span data-ttu-id="f3361-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f3361-104">SYNTAX</span></span>

### <span data-ttu-id="f3361-105">ApplicationObjectIdParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f3361-105">ApplicationObjectIdParameterSet (Default)</span></span>
```
Get-AzADAppCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3361-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3361-106">ApplicationIdParameterSet</span></span>
```
Get-AzADAppCredential -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3361-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3361-107">DisplayNameParameterSet</span></span>
```
Get-AzADAppCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3361-108">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3361-108">ApplicationObjectParameterSet</span></span>
```
Get-AzADAppCredential -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f3361-109">Opis</span><span class="sxs-lookup"><span data-stu-id="f3361-109">DESCRIPTION</span></span>
<span data-ttu-id="f3361-110">Polecenie cmdlet Get-AzADAppCredential może służyć do pobierania listy poświadczeń skojarzonych z aplikacją.</span><span class="sxs-lookup"><span data-stu-id="f3361-110">The Get-AzADAppCredential cmdlet can be used to retrieve a list of credentials associated with an application.</span></span>
<span data-ttu-id="f3361-111">To polecenie spowoduje pobranie wszystkich właściwości poświadczeń (ale nie wartości poświadczeń) skojarzonych z aplikacją.</span><span class="sxs-lookup"><span data-stu-id="f3361-111">This command will retrieve all of the credential properties (but not the credential value) associated with the application.</span></span>

## <span data-ttu-id="f3361-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f3361-112">EXAMPLES</span></span>

### <span data-ttu-id="f3361-113">Przykład 1: Uzyskaj poświadczenia aplikacji według identyfikatora obiektu</span><span class="sxs-lookup"><span data-stu-id="f3361-113">Example 1: Get application credentials by object id</span></span>

```powershell
PS C:\> Get-AzADAppCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
```

<span data-ttu-id="f3361-114">Zwraca listę poświadczeń skojarzonych z aplikacją o identyfikatorze obiektu "1f99cf81-0146-4f4e-beae-2007d0668476".</span><span class="sxs-lookup"><span data-stu-id="f3361-114">Returns a list of credentials associated with the application having object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

### <span data-ttu-id="f3361-115">Przykład 2: uzyskiwanie poświadczeń aplikacji według połączeń rurowych</span><span class="sxs-lookup"><span data-stu-id="f3361-115">Example 2: Get application credentials by piping</span></span>

```powershell
PS C:\> Get-AzADApplication -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 | Get-AzADAppCredential
```

<span data-ttu-id="f3361-116">Pobiera aplikację o identyfikatorze obiektu "1f99cf81-0146-4f4e-beae-2007d0668476" i przekazuje ją do polecenia cmdlet Get-AzADAppCredential, aby wyświetlić wszystkie poświadczenia dla tej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f3361-116">Gets the application with object id '1f99cf81-0146-4f4e-beae-2007d0668476' and pipes it to the Get-AzADAppCredential cmdlet to list all of the credentials for that application.</span></span>

## <span data-ttu-id="f3361-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f3361-117">PARAMETERS</span></span>

### <span data-ttu-id="f3361-118">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="f3361-118">-ApplicationId</span></span>
<span data-ttu-id="f3361-119">Identyfikator aplikacji, z której mają być pobierane poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="f3361-119">The id of the application to retrieve credentials from.</span></span>

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

### <span data-ttu-id="f3361-120">-Applicationobject</span><span class="sxs-lookup"><span data-stu-id="f3361-120">-ApplicationObject</span></span>
<span data-ttu-id="f3361-121">Obiekt aplikacji, z którego mają zostać pobrane poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="f3361-121">The application object to retrieve credentials from.</span></span>

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

### <span data-ttu-id="f3361-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3361-122">-DefaultProfile</span></span>
<span data-ttu-id="f3361-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="f3361-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f3361-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f3361-124">-DisplayName</span></span>
<span data-ttu-id="f3361-125">Nazwa wyświetlana aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f3361-125">The display name of the application.</span></span>

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

### <span data-ttu-id="f3361-126">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="f3361-126">-ObjectId</span></span>
<span data-ttu-id="f3361-127">Identyfikator obiektu aplikacji, z której mają być pobierane poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="f3361-127">The object id of the application to retrieve credentials from.</span></span>

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

### <span data-ttu-id="f3361-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3361-128">CommonParameters</span></span>
<span data-ttu-id="f3361-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3361-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3361-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f3361-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3361-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f3361-131">INPUTS</span></span>

### <span data-ttu-id="f3361-132">System. String</span><span class="sxs-lookup"><span data-stu-id="f3361-132">System.String</span></span>

### <span data-ttu-id="f3361-133">System. GUID</span><span class="sxs-lookup"><span data-stu-id="f3361-133">System.Guid</span></span>

### <span data-ttu-id="f3361-134">Microsoft. Azure. Commands. pozycji. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="f3361-134">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="f3361-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f3361-135">OUTPUTS</span></span>

### <span data-ttu-id="f3361-136">Microsoft. Azure. Commands. pozycji. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="f3361-136">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="f3361-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f3361-137">NOTES</span></span>

## <span data-ttu-id="f3361-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f3361-138">RELATED LINKS</span></span>

[<span data-ttu-id="f3361-139">Nowe — AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="f3361-139">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="f3361-140">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="f3361-140">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

[<span data-ttu-id="f3361-141">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="f3361-141">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

