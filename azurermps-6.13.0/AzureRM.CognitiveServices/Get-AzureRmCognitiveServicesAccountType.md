---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/get-azurermcognitiveservicesaccounttype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountType.md
ms.openlocfilehash: 05a4af3e92febcf30d44de9b114972a7c1f61d5b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550327"
---
# <span data-ttu-id="0e721-101">Get-AzureRmCognitiveServicesAccountType</span><span class="sxs-lookup"><span data-stu-id="0e721-101">Get-AzureRmCognitiveServicesAccountType</span></span>

## <span data-ttu-id="0e721-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0e721-102">SYNOPSIS</span></span>
<span data-ttu-id="0e721-103">Pobiera dostępne typy kont usług poznawczych.</span><span class="sxs-lookup"><span data-stu-id="0e721-103">Gets the available Cognitive Services Account Types.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e721-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0e721-104">SYNTAX</span></span>

### <span data-ttu-id="0e721-105">GetAccountTypeWithName</span><span class="sxs-lookup"><span data-stu-id="0e721-105">GetAccountTypeWithName</span></span>
```
Get-AzureRmCognitiveServicesAccountType -TypeName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0e721-106">GetAccountTypes</span><span class="sxs-lookup"><span data-stu-id="0e721-106">GetAccountTypes</span></span>
```
Get-AzureRmCognitiveServicesAccountType [-Location <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0e721-107">Opis</span><span class="sxs-lookup"><span data-stu-id="0e721-107">DESCRIPTION</span></span>
<span data-ttu-id="0e721-108">Polecenie cmdlet **Get-AzureRmCognitiveServicesAccountType** Pobiera dostępne typy konta usług poznawczych w ramach tej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="0e721-108">The **Get-AzureRmCognitiveServicesAccountType** cmdlet gets the available Cognitive Services Account Types under this subscription.</span></span>

## <span data-ttu-id="0e721-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0e721-109">EXAMPLES</span></span>

### <span data-ttu-id="0e721-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0e721-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmCognitiveServicesAccountType
```

<span data-ttu-id="0e721-111">Pobierz listę dostępnych typów.</span><span class="sxs-lookup"><span data-stu-id="0e721-111">Get the list of available Types.</span></span>

### <span data-ttu-id="0e721-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="0e721-112">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmCognitiveServicesAccountType -Location westus
```

<span data-ttu-id="0e721-113">Pobierz listę dostępnych typów w zachód.</span><span class="sxs-lookup"><span data-stu-id="0e721-113">Get the list of available Types in westus.</span></span>

### <span data-ttu-id="0e721-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="0e721-114">Example 3</span></span>
```powershell
PS C:\> Get-AzureRmCognitiveServicesAccountType -TypeName Face

Face
```

<span data-ttu-id="0e721-115">Sprawdź `Face` , czy jest to prawidłowa nazwa typu, czy nazwa będzie zwracana, jeśli jest to prawidłowa nazwa.</span><span class="sxs-lookup"><span data-stu-id="0e721-115">Check if `Face` is a valid Type name, the name will be returned if it is a valid name.</span></span>

## <span data-ttu-id="0e721-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0e721-116">PARAMETERS</span></span>

### <span data-ttu-id="0e721-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e721-117">-DefaultProfile</span></span>
<span data-ttu-id="0e721-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0e721-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e721-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="0e721-119">-Location</span></span>
<span data-ttu-id="0e721-120">Lokalizacja konta usług poznawczych.</span><span class="sxs-lookup"><span data-stu-id="0e721-120">Cognitive Services Account Location.</span></span>

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

### <span data-ttu-id="0e721-121">-TypeName</span><span class="sxs-lookup"><span data-stu-id="0e721-121">-TypeName</span></span>
<span data-ttu-id="0e721-122">Nazwa typu konta usług poznawczych.</span><span class="sxs-lookup"><span data-stu-id="0e721-122">Cognitive Services Account Type Name.</span></span>

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

### <span data-ttu-id="0e721-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e721-123">CommonParameters</span></span>
<span data-ttu-id="0e721-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e721-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e721-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e721-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e721-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0e721-126">INPUTS</span></span>

### <span data-ttu-id="0e721-127">System. String</span><span class="sxs-lookup"><span data-stu-id="0e721-127">System.String</span></span>

## <span data-ttu-id="0e721-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0e721-128">OUTPUTS</span></span>

### <span data-ttu-id="0e721-129">System. String []</span><span class="sxs-lookup"><span data-stu-id="0e721-129">System.String[]</span></span>

### <span data-ttu-id="0e721-130">System. String</span><span class="sxs-lookup"><span data-stu-id="0e721-130">System.String</span></span>

## <span data-ttu-id="0e721-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0e721-131">NOTES</span></span>

## <span data-ttu-id="0e721-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0e721-132">RELATED LINKS</span></span>
