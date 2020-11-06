---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6AC9DA05-756D-4D59-BD97-DBAAFBB3C7AC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADAppCredential.md
ms.openlocfilehash: fa2368e1982e66d8edecc465d1f6ded3a3d75205
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544139"
---
# <span data-ttu-id="aae2d-101">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="aae2d-101">Get-AzureRmADAppCredential</span></span>

## <span data-ttu-id="aae2d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="aae2d-102">SYNOPSIS</span></span>
<span data-ttu-id="aae2d-103">Pobiera listę poświadczeń skojarzonych z aplikacją.</span><span class="sxs-lookup"><span data-stu-id="aae2d-103">Retrieves a list of credentials associated with an application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aae2d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="aae2d-104">SYNTAX</span></span>

### <span data-ttu-id="aae2d-105">ApplicationObjectIdParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="aae2d-105">ApplicationObjectIdParameterSet (Default)</span></span>
```
Get-AzureRmADAppCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aae2d-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="aae2d-106">ApplicationIdParameterSet</span></span>
```
Get-AzureRmADAppCredential -ApplicationId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aae2d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="aae2d-107">DESCRIPTION</span></span>
<span data-ttu-id="aae2d-108">Polecenie cmdlet Get-AzureRmADAppCredential może służyć do pobierania listy poświadczeń skojarzonych z aplikacją.</span><span class="sxs-lookup"><span data-stu-id="aae2d-108">The Get-AzureRmADAppCredential cmdlet can be used to retrieve a list of credentials associated with an application.</span></span>

<span data-ttu-id="aae2d-109">To polecenie spowoduje pobranie wszystkich właściwości poświadczeń (ale nie wartości poświadczeń) skojarzonych z aplikacją.</span><span class="sxs-lookup"><span data-stu-id="aae2d-109">This command will retrieve all of the credential properties (but not the credential value) associated with the application.</span></span>

## <span data-ttu-id="aae2d-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="aae2d-110">EXAMPLES</span></span>

### <span data-ttu-id="aae2d-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="aae2d-111">Example 1</span></span>
```
PS E:\> Get-AzureRmADAppCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
```

<span data-ttu-id="aae2d-112">Zwraca listę poświadczeń skojarzonych z aplikacją o identyfikatorze obiektu "1f99cf81-0146-4f4e-beae-2007d0668476".</span><span class="sxs-lookup"><span data-stu-id="aae2d-112">Returns a list of credentials associated with the application having object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

## <span data-ttu-id="aae2d-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="aae2d-113">PARAMETERS</span></span>

### <span data-ttu-id="aae2d-114">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="aae2d-114">-ApplicationId</span></span>
<span data-ttu-id="aae2d-115">Identyfikator aplikacji, z której mają być pobierane poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="aae2d-115">The id of the application to retrieve credentials from.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aae2d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aae2d-116">-DefaultProfile</span></span>
<span data-ttu-id="aae2d-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="aae2d-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aae2d-118">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="aae2d-118">-ObjectId</span></span>
<span data-ttu-id="aae2d-119">Identyfikator obiektu aplikacji, z której mają być pobierane poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="aae2d-119">The object id of the application to retrieve credentials from.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aae2d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aae2d-120">CommonParameters</span></span>
<span data-ttu-id="aae2d-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aae2d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aae2d-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aae2d-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aae2d-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aae2d-123">INPUTS</span></span>

### <span data-ttu-id="aae2d-124">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="aae2d-124">None</span></span>
<span data-ttu-id="aae2d-125">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="aae2d-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="aae2d-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="aae2d-126">OUTPUTS</span></span>

### <span data-ttu-id="aae2d-127">Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="aae2d-127">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="aae2d-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="aae2d-128">NOTES</span></span>

## <span data-ttu-id="aae2d-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aae2d-129">RELATED LINKS</span></span>

[<span data-ttu-id="aae2d-130">Nowe — AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="aae2d-130">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="aae2d-131">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="aae2d-131">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

[<span data-ttu-id="aae2d-132">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="aae2d-132">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

