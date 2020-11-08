---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccounttype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountType.md
ms.openlocfilehash: a99ca4bb636ba1767fc5f50611d3c5a9eb991312
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051089"
---
# <span data-ttu-id="a92da-101">Get-AzCognitiveServicesAccountType</span><span class="sxs-lookup"><span data-stu-id="a92da-101">Get-AzCognitiveServicesAccountType</span></span>

## <span data-ttu-id="a92da-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a92da-102">SYNOPSIS</span></span>
<span data-ttu-id="a92da-103">Pobiera dostępne typy kont usług poznawczych.</span><span class="sxs-lookup"><span data-stu-id="a92da-103">Gets the available Cognitive Services Account Types.</span></span>

## <span data-ttu-id="a92da-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a92da-104">SYNTAX</span></span>

### <span data-ttu-id="a92da-105">GetAccountTypes (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a92da-105">GetAccountTypes (Default)</span></span>
```
Get-AzCognitiveServicesAccountType [-Location <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a92da-106">GetAccountTypeWithName</span><span class="sxs-lookup"><span data-stu-id="a92da-106">GetAccountTypeWithName</span></span>
```
Get-AzCognitiveServicesAccountType -TypeName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a92da-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a92da-107">DESCRIPTION</span></span>
<span data-ttu-id="a92da-108">Polecenie cmdlet **Get-AzCognitiveServicesAccountType** Pobiera dostępne typy konta usług poznawczych w ramach tej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="a92da-108">The **Get-AzCognitiveServicesAccountType** cmdlet gets the available Cognitive Services Account Types under this subscription.</span></span>

## <span data-ttu-id="a92da-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a92da-109">EXAMPLES</span></span>

### <span data-ttu-id="a92da-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a92da-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountType
```

<span data-ttu-id="a92da-111">Pobierz listę dostępnych typów.</span><span class="sxs-lookup"><span data-stu-id="a92da-111">Get the list of available Types.</span></span>

### <span data-ttu-id="a92da-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a92da-112">Example 2</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountType -Location westus
```

<span data-ttu-id="a92da-113">Pobierz listę dostępnych typów w zachód.</span><span class="sxs-lookup"><span data-stu-id="a92da-113">Get the list of available Types in westus.</span></span>

### <span data-ttu-id="a92da-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="a92da-114">Example 3</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountType -TypeName Face

Face
```

<span data-ttu-id="a92da-115">Sprawdź `Face` , czy jest to prawidłowa nazwa typu, czy nazwa będzie zwracana, jeśli jest to prawidłowa nazwa.</span><span class="sxs-lookup"><span data-stu-id="a92da-115">Check if `Face` is a valid Type name, the name will be returned if it is a valid name.</span></span>

## <span data-ttu-id="a92da-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a92da-116">PARAMETERS</span></span>

### <span data-ttu-id="a92da-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a92da-117">-DefaultProfile</span></span>
<span data-ttu-id="a92da-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a92da-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a92da-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="a92da-119">-Location</span></span>
<span data-ttu-id="a92da-120">Lokalizacja konta usług poznawczych.</span><span class="sxs-lookup"><span data-stu-id="a92da-120">Cognitive Services Account Location.</span></span>

```yaml
Type: System.String
Parameter Sets: GetAccountTypes
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a92da-121">-TypeName</span><span class="sxs-lookup"><span data-stu-id="a92da-121">-TypeName</span></span>
<span data-ttu-id="a92da-122">Nazwa typu konta usług poznawczych.</span><span class="sxs-lookup"><span data-stu-id="a92da-122">Cognitive Services Account Type Name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetAccountTypeWithName
Aliases: CognitiveServicesAccountTypeName, AccountTypeName, KindName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a92da-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a92da-123">CommonParameters</span></span>
<span data-ttu-id="a92da-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a92da-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a92da-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a92da-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a92da-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a92da-126">INPUTS</span></span>

### <span data-ttu-id="a92da-127">System. String</span><span class="sxs-lookup"><span data-stu-id="a92da-127">System.String</span></span>

## <span data-ttu-id="a92da-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a92da-128">OUTPUTS</span></span>

### <span data-ttu-id="a92da-129">System. String []</span><span class="sxs-lookup"><span data-stu-id="a92da-129">System.String[]</span></span>

### <span data-ttu-id="a92da-130">System. String</span><span class="sxs-lookup"><span data-stu-id="a92da-130">System.String</span></span>

## <span data-ttu-id="a92da-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a92da-131">NOTES</span></span>

## <span data-ttu-id="a92da-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a92da-132">RELATED LINKS</span></span>
