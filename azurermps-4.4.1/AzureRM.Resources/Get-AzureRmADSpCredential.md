---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 7690143F-5F09-4739-9F66-B2ACDF8305F4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADSpCredential.md
ms.openlocfilehash: 247b0735e41f02a55b94e5a8f8ed44136eb3f37e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527321"
---
# <span data-ttu-id="9d421-101">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="9d421-101">Get-AzureRmADSpCredential</span></span>

## <span data-ttu-id="9d421-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9d421-102">SYNOPSIS</span></span>
<span data-ttu-id="9d421-103">Pobiera listę poświadczeń skojarzonych z podmiotem zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="9d421-103">Retrieves a list of credentials associated with a service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d421-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9d421-104">SYNTAX</span></span>

### <span data-ttu-id="9d421-105">ObjectIdParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9d421-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzureRmADSpCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d421-106">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d421-106">SPNParameterSet</span></span>
```
Get-AzureRmADSpCredential -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9d421-107">Opis</span><span class="sxs-lookup"><span data-stu-id="9d421-107">DESCRIPTION</span></span>
<span data-ttu-id="9d421-108">Polecenie cmdlet Get-AzureRmADSpCredential może służyć do pobierania listy poświadczeń skojarzonych z podmiotem zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="9d421-108">The Get-AzureRmADSpCredential cmdlet can be used to retrieve a list of credentials associated with a service principal.</span></span>
<span data-ttu-id="9d421-109">To polecenie spowoduje pobranie wszystkich właściwości poświadczeń (ale nie wartości poświadczeń) skojarzonych z podmiotem zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="9d421-109">This command will retrieve all of the credential properties (but not the credential value) associated with the service principal.</span></span>

## <span data-ttu-id="9d421-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9d421-110">EXAMPLES</span></span>

### <span data-ttu-id="9d421-111">--------------------------Przykład 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="9d421-111">--------------------------  Example 1  --------------------------</span></span>
```
PS E:\> Get-AzureRmADSpCredential -ServicePrincipalName http://test12345
```

<span data-ttu-id="9d421-112">Zwraca listę poświadczeń skojarzonych z podmiotem zabezpieczeń usługi posiadającym nazwę SPN " http://test12345 ".</span><span class="sxs-lookup"><span data-stu-id="9d421-112">Returns a list of credentials associated with the service principal having SPN 'http://test12345'.</span></span>

## <span data-ttu-id="9d421-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9d421-113">PARAMETERS</span></span>

### <span data-ttu-id="9d421-114">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="9d421-114">-ObjectId</span></span>
<span data-ttu-id="9d421-115">Identyfikator obiektu podmiotu usługi, z którego mają być pobierane poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="9d421-115">The object id of the service principal to retrieve credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d421-116">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="9d421-116">-ServicePrincipalName</span></span>
<span data-ttu-id="9d421-117">Nazwa (SPN) podmiotu zabezpieczeń usługi, z którego mają być pobierane poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="9d421-117">The name (SPN) of the service principal to retrieve credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d421-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d421-118">-DefaultProfile</span></span>
<span data-ttu-id="9d421-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9d421-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d421-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d421-120">CommonParameters</span></span>
<span data-ttu-id="9d421-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d421-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d421-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d421-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d421-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9d421-123">INPUTS</span></span>

## <span data-ttu-id="9d421-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9d421-124">OUTPUTS</span></span>

### <span data-ttu-id="9d421-125">Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="9d421-125">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="9d421-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9d421-126">NOTES</span></span>

## <span data-ttu-id="9d421-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9d421-127">RELATED LINKS</span></span>

[<span data-ttu-id="9d421-128">Nowe — AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="9d421-128">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="9d421-129">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="9d421-129">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)

[<span data-ttu-id="9d421-130">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="9d421-130">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

