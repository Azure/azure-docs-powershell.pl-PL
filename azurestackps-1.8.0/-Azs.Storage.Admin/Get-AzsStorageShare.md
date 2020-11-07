---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: cc6e2adff73e4b7c81a401bb98e9ab625005ae3f
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2020
ms.locfileid: "93889105"
---
# <span data-ttu-id="3a677-101">Get-AzsStorageShare</span><span class="sxs-lookup"><span data-stu-id="3a677-101">Get-AzsStorageShare</span></span>

## <span data-ttu-id="3a677-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3a677-102">SYNOPSIS</span></span>
<span data-ttu-id="3a677-103">Zwraca listę udziałów w magazynie.</span><span class="sxs-lookup"><span data-stu-id="3a677-103">Returns a list of storage shares.</span></span>

## <span data-ttu-id="3a677-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3a677-104">SYNTAX</span></span>

### <span data-ttu-id="3a677-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="3a677-105">List (Default)</span></span>
```
Get-AzsStorageShare -FarmName <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="3a677-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="3a677-106">Get</span></span>
```
Get-AzsStorageShare -FarmName <String> -Name <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="3a677-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="3a677-107">ResourceId</span></span>
```
Get-AzsStorageShare -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="3a677-108">Opis</span><span class="sxs-lookup"><span data-stu-id="3a677-108">DESCRIPTION</span></span>
<span data-ttu-id="3a677-109">Zwraca listę udziałów w magazynie.</span><span class="sxs-lookup"><span data-stu-id="3a677-109">Returns a list of storage shares.</span></span>

## <span data-ttu-id="3a677-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3a677-110">EXAMPLES</span></span>

### <span data-ttu-id="3a677-111">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="3a677-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageShare -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="3a677-112">Pobierz listę udziałów w magazynie.</span><span class="sxs-lookup"><span data-stu-id="3a677-112">Get the list of storage shares.</span></span>

## <span data-ttu-id="3a677-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3a677-113">PARAMETERS</span></span>

### <span data-ttu-id="3a677-114">-Farmname</span><span class="sxs-lookup"><span data-stu-id="3a677-114">-FarmName</span></span>
<span data-ttu-id="3a677-115">Identyfikator farmy.</span><span class="sxs-lookup"><span data-stu-id="3a677-115">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a677-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3a677-116">-Name</span></span>
<span data-ttu-id="3a677-117">Nazwa udziału.</span><span class="sxs-lookup"><span data-stu-id="3a677-117">Share name.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: ShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a677-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a677-118">-ResourceGroupName</span></span>
<span data-ttu-id="3a677-119">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3a677-119">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a677-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3a677-120">-ResourceId</span></span>
<span data-ttu-id="3a677-121">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="3a677-121">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a677-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a677-122">CommonParameters</span></span>
<span data-ttu-id="3a677-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a677-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a677-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a677-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a677-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3a677-125">INPUTS</span></span>

## <span data-ttu-id="3a677-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3a677-126">OUTPUTS</span></span>

### <span data-ttu-id="3a677-127">Microsoft. AzureStack. Management. Storage. admin. models. Share</span><span class="sxs-lookup"><span data-stu-id="3a677-127">Microsoft.AzureStack.Management.Storage.Admin.Models.Share</span></span>

## <span data-ttu-id="3a677-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3a677-128">NOTES</span></span>

## <span data-ttu-id="3a677-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3a677-129">RELATED LINKS</span></span>

