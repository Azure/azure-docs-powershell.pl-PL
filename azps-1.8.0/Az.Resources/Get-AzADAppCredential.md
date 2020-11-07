---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6AC9DA05-756D-4D59-BD97-DBAAFBB3C7AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADAppCredential.md
ms.openlocfilehash: fdef07255316b1d7529202c36b844e8732c76390
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708430"
---
# <span data-ttu-id="45fb5-101">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="45fb5-101">Get-AzADAppCredential</span></span>

## <span data-ttu-id="45fb5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="45fb5-102">SYNOPSIS</span></span>
<span data-ttu-id="45fb5-103">Pobiera listę poświadczeń skojarzonych z aplikacją.</span><span class="sxs-lookup"><span data-stu-id="45fb5-103">Retrieves a list of credentials associated with an application.</span></span>

## <span data-ttu-id="45fb5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="45fb5-104">SYNTAX</span></span>

### <span data-ttu-id="45fb5-105">ApplicationObjectIdParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="45fb5-105">ApplicationObjectIdParameterSet (Default)</span></span>
```
Get-AzADAppCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45fb5-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="45fb5-106">ApplicationIdParameterSet</span></span>
```
Get-AzADAppCredential -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45fb5-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="45fb5-107">DisplayNameParameterSet</span></span>
```
Get-AzADAppCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45fb5-108">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="45fb5-108">ApplicationObjectParameterSet</span></span>
```
Get-AzADAppCredential -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="45fb5-109">Opis</span><span class="sxs-lookup"><span data-stu-id="45fb5-109">DESCRIPTION</span></span>
<span data-ttu-id="45fb5-110">Polecenie cmdlet Get-AzADAppCredential może służyć do pobierania listy poświadczeń skojarzonych z aplikacją.</span><span class="sxs-lookup"><span data-stu-id="45fb5-110">The Get-AzADAppCredential cmdlet can be used to retrieve a list of credentials associated with an application.</span></span>
<span data-ttu-id="45fb5-111">To polecenie spowoduje pobranie wszystkich właściwości poświadczeń (ale nie wartości poświadczeń) skojarzonych z aplikacją.</span><span class="sxs-lookup"><span data-stu-id="45fb5-111">This command will retrieve all of the credential properties (but not the credential value) associated with the application.</span></span>

## <span data-ttu-id="45fb5-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="45fb5-112">EXAMPLES</span></span>

### <span data-ttu-id="45fb5-113">Przykład 1-Uzyskaj poświadczenia aplikacji według identyfikatora obiektu</span><span class="sxs-lookup"><span data-stu-id="45fb5-113">Example 1 - Get application credentials by object id</span></span>

```
PS C:\> Get-AzADAppCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
```

<span data-ttu-id="45fb5-114">Zwraca listę poświadczeń skojarzonych z aplikacją o identyfikatorze obiektu "1f99cf81-0146-4f4e-beae-2007d0668476".</span><span class="sxs-lookup"><span data-stu-id="45fb5-114">Returns a list of credentials associated with the application having object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

### <span data-ttu-id="45fb5-115">Przykład 2 — Uzyskaj poświadczenia aplikacji według połączeń rurowych</span><span class="sxs-lookup"><span data-stu-id="45fb5-115">Example 2 - Get application credentials by piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 | Get-AzADAppCredential
```

<span data-ttu-id="45fb5-116">Pobiera aplikację o identyfikatorze obiektu "1f99cf81-0146-4f4e-beae-2007d0668476" i przekazuje ją do polecenia cmdlet Get-AzADAppCredential, aby wyświetlić wszystkie poświadczenia dla tej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="45fb5-116">Gets the application with object id '1f99cf81-0146-4f4e-beae-2007d0668476' and pipes it to the Get-AzADAppCredential cmdlet to list all of the credentials for that application.</span></span>

## <span data-ttu-id="45fb5-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="45fb5-117">PARAMETERS</span></span>

### <span data-ttu-id="45fb5-118">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="45fb5-118">-ApplicationId</span></span>
<span data-ttu-id="45fb5-119">Identyfikator aplikacji, z której mają być pobierane poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="45fb5-119">The id of the application to retrieve credentials from.</span></span>

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

### <span data-ttu-id="45fb5-120">-Applicationobject</span><span class="sxs-lookup"><span data-stu-id="45fb5-120">-ApplicationObject</span></span>
<span data-ttu-id="45fb5-121">Obiekt aplikacji, z którego mają zostać pobrane poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="45fb5-121">The application object to retrieve credentials from.</span></span>

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

### <span data-ttu-id="45fb5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45fb5-122">-DefaultProfile</span></span>
<span data-ttu-id="45fb5-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="45fb5-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="45fb5-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="45fb5-124">-DisplayName</span></span>
<span data-ttu-id="45fb5-125">Nazwa wyświetlana aplikacji.</span><span class="sxs-lookup"><span data-stu-id="45fb5-125">The display name of the application.</span></span>

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

### <span data-ttu-id="45fb5-126">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="45fb5-126">-ObjectId</span></span>
<span data-ttu-id="45fb5-127">Identyfikator obiektu aplikacji, z której mają być pobierane poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="45fb5-127">The object id of the application to retrieve credentials from.</span></span>

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

### <span data-ttu-id="45fb5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45fb5-128">CommonParameters</span></span>
<span data-ttu-id="45fb5-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45fb5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45fb5-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45fb5-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45fb5-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="45fb5-131">INPUTS</span></span>

### <span data-ttu-id="45fb5-132">System. String</span><span class="sxs-lookup"><span data-stu-id="45fb5-132">System.String</span></span>

### <span data-ttu-id="45fb5-133">System. GUID</span><span class="sxs-lookup"><span data-stu-id="45fb5-133">System.Guid</span></span>

### <span data-ttu-id="45fb5-134">Microsoft. Azure. Commands. pozycji. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="45fb5-134">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="45fb5-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="45fb5-135">OUTPUTS</span></span>

### <span data-ttu-id="45fb5-136">Microsoft. Azure. Commands. pozycji. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="45fb5-136">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="45fb5-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="45fb5-137">NOTES</span></span>

## <span data-ttu-id="45fb5-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="45fb5-138">RELATED LINKS</span></span>

[<span data-ttu-id="45fb5-139">Nowe — AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="45fb5-139">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="45fb5-140">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="45fb5-140">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

[<span data-ttu-id="45fb5-141">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="45fb5-141">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

