---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 7690143F-5F09-4739-9F66-B2ACDF8305F4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADSpCredential.md
ms.openlocfilehash: 8c03dd19fd2995347a3b4ae52de04fdcb3f02c30
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717314"
---
# <span data-ttu-id="1fae5-101">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="1fae5-101">Get-AzureRmADSpCredential</span></span>

## <span data-ttu-id="1fae5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1fae5-102">SYNOPSIS</span></span>
<span data-ttu-id="1fae5-103">Pobiera listę poświadczeń skojarzonych z podmiotem zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="1fae5-103">Retrieves a list of credentials associated with a service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1fae5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1fae5-104">SYNTAX</span></span>

### <span data-ttu-id="1fae5-105">ObjectIdParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1fae5-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzureRmADSpCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1fae5-106">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="1fae5-106">SPNParameterSet</span></span>
```
Get-AzureRmADSpCredential -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1fae5-107">Opis</span><span class="sxs-lookup"><span data-stu-id="1fae5-107">DESCRIPTION</span></span>
<span data-ttu-id="1fae5-108">Polecenie cmdlet Get-AzureRmADSpCredential może służyć do pobierania listy poświadczeń skojarzonych z podmiotem zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="1fae5-108">The Get-AzureRmADSpCredential cmdlet can be used to retrieve a list of credentials associated with a service principal.</span></span>
<span data-ttu-id="1fae5-109">To polecenie spowoduje pobranie wszystkich właściwości poświadczeń (ale nie wartości poświadczeń) skojarzonych z podmiotem zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="1fae5-109">This command will retrieve all of the credential properties (but not the credential value) associated with the service principal.</span></span>

## <span data-ttu-id="1fae5-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1fae5-110">EXAMPLES</span></span>

### <span data-ttu-id="1fae5-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1fae5-111">Example 1</span></span>
```
PS E:\> Get-AzureRmADSpCredential -ServicePrincipalName http://test12345
```

<span data-ttu-id="1fae5-112">Zwraca listę poświadczeń skojarzonych z podmiotem zabezpieczeń usługi posiadającym nazwę SPN " http://test12345 ".</span><span class="sxs-lookup"><span data-stu-id="1fae5-112">Returns a list of credentials associated with the service principal having SPN 'http://test12345'.</span></span>

## <span data-ttu-id="1fae5-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1fae5-113">PARAMETERS</span></span>

### <span data-ttu-id="1fae5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fae5-114">-DefaultProfile</span></span>
<span data-ttu-id="1fae5-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="1fae5-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1fae5-116">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="1fae5-116">-ObjectId</span></span>
<span data-ttu-id="1fae5-117">Identyfikator obiektu podmiotu usługi, z którego mają być pobierane poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="1fae5-117">The object id of the service principal to retrieve credentials from.</span></span>

```yaml
Type: String
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fae5-118">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="1fae5-118">-ServicePrincipalName</span></span>
<span data-ttu-id="1fae5-119">Nazwa (SPN) podmiotu zabezpieczeń usługi, z którego mają być pobierane poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="1fae5-119">The name (SPN) of the service principal to retrieve credentials from.</span></span>

```yaml
Type: String
Parameter Sets: SPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fae5-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fae5-120">CommonParameters</span></span>
<span data-ttu-id="1fae5-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fae5-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fae5-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fae5-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fae5-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1fae5-123">INPUTS</span></span>

### <span data-ttu-id="1fae5-124">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="1fae5-124">None</span></span>
<span data-ttu-id="1fae5-125">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="1fae5-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1fae5-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1fae5-126">OUTPUTS</span></span>

### <span data-ttu-id="1fae5-127">Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="1fae5-127">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="1fae5-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1fae5-128">NOTES</span></span>

## <span data-ttu-id="1fae5-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1fae5-129">RELATED LINKS</span></span>

[<span data-ttu-id="1fae5-130">Nowe — AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="1fae5-130">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="1fae5-131">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="1fae5-131">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)

[<span data-ttu-id="1fae5-132">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="1fae5-132">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

