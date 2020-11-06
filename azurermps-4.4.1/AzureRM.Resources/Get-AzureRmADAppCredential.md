---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6AC9DA05-756D-4D59-BD97-DBAAFBB3C7AC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADAppCredential.md
ms.openlocfilehash: e270a59e3799302eed49a0fd60180bb8d4589d92
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553778"
---
# <span data-ttu-id="73188-101">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="73188-101">Get-AzureRmADAppCredential</span></span>

## <span data-ttu-id="73188-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="73188-102">SYNOPSIS</span></span>
<span data-ttu-id="73188-103">Pobiera listę poświadczeń skojarzonych z aplikacją.</span><span class="sxs-lookup"><span data-stu-id="73188-103">Retrieves a list of credentials associated with an application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73188-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="73188-104">SYNTAX</span></span>

### <span data-ttu-id="73188-105">ApplicationObjectIdParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="73188-105">ApplicationObjectIdParameterSet (Default)</span></span>
```
Get-AzureRmADAppCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73188-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="73188-106">ApplicationIdParameterSet</span></span>
```
Get-AzureRmADAppCredential -ApplicationId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="73188-107">Opis</span><span class="sxs-lookup"><span data-stu-id="73188-107">DESCRIPTION</span></span>
<span data-ttu-id="73188-108">Polecenie cmdlet Get-AzureRmADAppCredential może służyć do pobierania listy poświadczeń skojarzonych z aplikacją.</span><span class="sxs-lookup"><span data-stu-id="73188-108">The Get-AzureRmADAppCredential cmdlet can be used to retrieve a list of credentials associated with an application.</span></span>

<span data-ttu-id="73188-109">To polecenie spowoduje pobranie wszystkich właściwości poświadczeń (ale nie wartości poświadczeń) skojarzonych z aplikacją.</span><span class="sxs-lookup"><span data-stu-id="73188-109">This command will retrieve all of the credential properties (but not the credential value) associated with the application.</span></span>

## <span data-ttu-id="73188-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="73188-110">EXAMPLES</span></span>

### <span data-ttu-id="73188-111">--------------------------Przykład 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="73188-111">--------------------------  Example 1  --------------------------</span></span>
```
PS E:\> Get-AzureRmADAppCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
```

<span data-ttu-id="73188-112">Zwraca listę poświadczeń skojarzonych z aplikacją o identyfikatorze obiektu "1f99cf81-0146-4f4e-beae-2007d0668476".</span><span class="sxs-lookup"><span data-stu-id="73188-112">Returns a list of credentials associated with the application having object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

## <span data-ttu-id="73188-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="73188-113">PARAMETERS</span></span>

### <span data-ttu-id="73188-114">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="73188-114">-ApplicationId</span></span>
<span data-ttu-id="73188-115">Identyfikator aplikacji, z której mają być pobierane poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="73188-115">The id of the application to retrieve credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73188-116">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="73188-116">-ObjectId</span></span>
<span data-ttu-id="73188-117">Identyfikator obiektu aplikacji, z której mają być pobierane poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="73188-117">The object id of the application to retrieve credentials from.</span></span>

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

### <span data-ttu-id="73188-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73188-118">-DefaultProfile</span></span>
<span data-ttu-id="73188-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="73188-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73188-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73188-120">CommonParameters</span></span>
<span data-ttu-id="73188-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73188-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73188-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73188-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73188-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="73188-123">INPUTS</span></span>

## <span data-ttu-id="73188-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="73188-124">OUTPUTS</span></span>

### <span data-ttu-id="73188-125">Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="73188-125">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="73188-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="73188-126">NOTES</span></span>

## <span data-ttu-id="73188-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="73188-127">RELATED LINKS</span></span>

[<span data-ttu-id="73188-128">Nowe — AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="73188-128">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="73188-129">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="73188-129">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

[<span data-ttu-id="73188-130">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="73188-130">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

