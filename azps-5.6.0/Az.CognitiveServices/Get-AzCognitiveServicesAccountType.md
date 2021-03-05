---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccounttype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountType.md
ms.openlocfilehash: aacc24926bf38f52f1fd273847e48082c8d110c9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981217"
---
# <span data-ttu-id="e4e8c-101">Get-AzCognitiveServicesAccountType</span><span class="sxs-lookup"><span data-stu-id="e4e8c-101">Get-AzCognitiveServicesAccountType</span></span>

## <span data-ttu-id="e4e8c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4e8c-102">SYNOPSIS</span></span>
<span data-ttu-id="e4e8c-103">Pobiera dostępne typy kont usług Cognitive Services.</span><span class="sxs-lookup"><span data-stu-id="e4e8c-103">Gets the available Cognitive Services Account Types.</span></span>

## <span data-ttu-id="e4e8c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e4e8c-104">SYNTAX</span></span>

### <span data-ttu-id="e4e8c-105">GetAccountTypes (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="e4e8c-105">GetAccountTypes (Default)</span></span>
```
Get-AzCognitiveServicesAccountType [-Location <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e4e8c-106">GetAccountTypeWithName</span><span class="sxs-lookup"><span data-stu-id="e4e8c-106">GetAccountTypeWithName</span></span>
```
Get-AzCognitiveServicesAccountType -TypeName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e4e8c-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="e4e8c-107">DESCRIPTION</span></span>
<span data-ttu-id="e4e8c-108">Polecenie **cmdlet Get-AzCognitiveServicesAccountType** pobiera dostępne typy kont usług Cognitive Services w ramach tej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e4e8c-108">The **Get-AzCognitiveServicesAccountType** cmdlet gets the available Cognitive Services Account Types under this subscription.</span></span>

## <span data-ttu-id="e4e8c-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e4e8c-109">EXAMPLES</span></span>

### <span data-ttu-id="e4e8c-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e4e8c-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountType
```

<span data-ttu-id="e4e8c-111">Pobierz listę dostępnych typów.</span><span class="sxs-lookup"><span data-stu-id="e4e8c-111">Get the list of available Types.</span></span>

### <span data-ttu-id="e4e8c-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="e4e8c-112">Example 2</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountType -Location westus
```

<span data-ttu-id="e4e8c-113">Pobierz listę dostępnych typów w języku zachód.</span><span class="sxs-lookup"><span data-stu-id="e4e8c-113">Get the list of available Types in westus.</span></span>

### <span data-ttu-id="e4e8c-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="e4e8c-114">Example 3</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountType -TypeName Face

Face
```

<span data-ttu-id="e4e8c-115">Sprawdź, czy jest prawidłową nazwą typu, zostanie zwrócona, jeśli `Face` jest prawidłową nazwą.</span><span class="sxs-lookup"><span data-stu-id="e4e8c-115">Check if `Face` is a valid Type name, the name will be returned if it is a valid name.</span></span>

## <span data-ttu-id="e4e8c-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e4e8c-116">PARAMETERS</span></span>

### <span data-ttu-id="e4e8c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4e8c-117">-DefaultProfile</span></span>
<span data-ttu-id="e4e8c-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e4e8c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4e8c-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="e4e8c-119">-Location</span></span>
<span data-ttu-id="e4e8c-120">Lokalizacja konta usług Cognitive Services.</span><span class="sxs-lookup"><span data-stu-id="e4e8c-120">Cognitive Services Account Location.</span></span>

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

### <span data-ttu-id="e4e8c-121">-TypeName</span><span class="sxs-lookup"><span data-stu-id="e4e8c-121">-TypeName</span></span>
<span data-ttu-id="e4e8c-122">Nazwa typu konta usług Cognitive Services.</span><span class="sxs-lookup"><span data-stu-id="e4e8c-122">Cognitive Services Account Type Name.</span></span>

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

### <span data-ttu-id="e4e8c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4e8c-123">CommonParameters</span></span>
<span data-ttu-id="e4e8c-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4e8c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4e8c-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e4e8c-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4e8c-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e4e8c-126">INPUTS</span></span>

### <span data-ttu-id="e4e8c-127">System.String</span><span class="sxs-lookup"><span data-stu-id="e4e8c-127">System.String</span></span>

## <span data-ttu-id="e4e8c-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e4e8c-128">OUTPUTS</span></span>

### <span data-ttu-id="e4e8c-129">System.String[]</span><span class="sxs-lookup"><span data-stu-id="e4e8c-129">System.String[]</span></span>

### <span data-ttu-id="e4e8c-130">System.String</span><span class="sxs-lookup"><span data-stu-id="e4e8c-130">System.String</span></span>

## <span data-ttu-id="e4e8c-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e4e8c-131">NOTES</span></span>

## <span data-ttu-id="e4e8c-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e4e8c-132">RELATED LINKS</span></span>
