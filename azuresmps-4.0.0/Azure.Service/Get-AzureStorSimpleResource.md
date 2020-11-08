---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 482E8CD6-C38F-4BD5-8214-016D0D8C7FD0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6381b8e0fac5ebf047122f131af6087d5bb5a9fb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054520"
---
# <span data-ttu-id="cd3ba-101">Get-AzureStorSimpleResource</span><span class="sxs-lookup"><span data-stu-id="cd3ba-101">Get-AzureStorSimpleResource</span></span>

## <span data-ttu-id="cd3ba-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cd3ba-102">SYNOPSIS</span></span>
<span data-ttu-id="cd3ba-103">Pobiera wszystkie utworzone przez siebie zasoby.</span><span class="sxs-lookup"><span data-stu-id="cd3ba-103">Gets all resources that you created.</span></span>

## <span data-ttu-id="cd3ba-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cd3ba-104">SYNTAX</span></span>

```
Get-AzureStorSimpleResource [-ResourceName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="cd3ba-105">Opis</span><span class="sxs-lookup"><span data-stu-id="cd3ba-105">DESCRIPTION</span></span>
<span data-ttu-id="cd3ba-106">Polecenie cmdlet **Get-AzureStorSimpleResource** umożliwia pobieranie wszystkich zasobów utworzonych za pomocą portalu Azure Portal.</span><span class="sxs-lookup"><span data-stu-id="cd3ba-106">The **Get-AzureStorSimpleResource** cmdlet gets all resources that you created by using Azure Portal.</span></span>
<span data-ttu-id="cd3ba-107">Polecenie cmdlet umożliwia pobieranie szczegółów, których można użyć w celu nawiązania połączenia z zasobami.</span><span class="sxs-lookup"><span data-stu-id="cd3ba-107">The cmdlet gets details you can use to connect to the resources.</span></span>

## <span data-ttu-id="cd3ba-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cd3ba-108">EXAMPLES</span></span>

### <span data-ttu-id="cd3ba-109">Przykład 1: pobieranie wszystkich zasobów</span><span class="sxs-lookup"><span data-stu-id="cd3ba-109">Example 1: Get all resources</span></span>
```
PS C:\>Get-AzureStorSimpleResource
VERBOSE: ClientRequestId: 5cd61b91-ef40-43b4-986d-156e06d2ed65_PS

ResourceName                                      ResourceId           ResourceState
------------                                      ----------           -------------
Contoso63-Tsqa                                    8838459798595306468  Started
Contoso68-Tsqa                                    2859070203638134681  Started
Contoso73-Tsqa                                    7871392677286863733  Started
Contoso87-Tsqa                                    1909806764156522689  Started
VERBOSE: Found 4 StorSimple resources.
```

<span data-ttu-id="cd3ba-110">To polecenie umożliwia pobieranie wszystkich utworzonych zasobów.</span><span class="sxs-lookup"><span data-stu-id="cd3ba-110">This command gets all the resources you created.</span></span>
<span data-ttu-id="cd3ba-111">W tym przykładzie występują trzy zasoby.</span><span class="sxs-lookup"><span data-stu-id="cd3ba-111">In this example, there are three resources.</span></span>

### <span data-ttu-id="cd3ba-112">Przykład 2: Pobieranie zasobu przy użyciu jego nazwy</span><span class="sxs-lookup"><span data-stu-id="cd3ba-112">Example 2: Get a resource by using its name</span></span>
```
PS C:\>Get-AzureStorSimpleResource -ResourceName "Contoso63-Tsqa"
VERBOSE: ClientRequestId: efc3c85c-12aa-4345-b6eb-ccc532de4825_PS

ResourceName                                      ResourceId           ResourceState
------------                                      ----------           -------------
Contoso63-Tsqa                                    1909806764156522689  Started
VERBOSE: Found 1 StorSimple resource.
```

<span data-ttu-id="cd3ba-113">To polecenie uzyskuje zasób o nazwie Contoso63-Tsqa.</span><span class="sxs-lookup"><span data-stu-id="cd3ba-113">This command gets the resource named Contoso63-Tsqa.</span></span>

### <span data-ttu-id="cd3ba-114">Przykład 3: próba uzyskania nieistniejącego zasobu</span><span class="sxs-lookup"><span data-stu-id="cd3ba-114">Example 3: Attempt to get a nonexistent resource</span></span>
```
PS C:\>Get-AzureStorSimpleResource -ResourceName "Contoso64-Tsqa"
VERBOSE: ClientRequestId: 5d08d40b-f9d7-4d43-956f-13f01e89625b_PS
VERBOSE: Invalid input : Could not find a resource named Contoso64-Tsqa in your subscription.
```

<span data-ttu-id="cd3ba-115">To polecenie próbuje uzyskać zasób o nazwie Contoso64-Tsqa.</span><span class="sxs-lookup"><span data-stu-id="cd3ba-115">This command attempts to get the resource named Contoso64-Tsqa.</span></span>
<span data-ttu-id="cd3ba-116">Brak zasobu o tej nazwie.</span><span class="sxs-lookup"><span data-stu-id="cd3ba-116">There is no resource that has this name.</span></span>
<span data-ttu-id="cd3ba-117">W tym przykładzie nie są zwracane żadne zasoby.</span><span class="sxs-lookup"><span data-stu-id="cd3ba-117">This example does not return any resource.</span></span>

## <span data-ttu-id="cd3ba-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cd3ba-118">PARAMETERS</span></span>

### <span data-ttu-id="cd3ba-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="cd3ba-119">-Profile</span></span>
<span data-ttu-id="cd3ba-120">Określa Profil platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="cd3ba-120">Specifies an Azure profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd3ba-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="cd3ba-121">-ResourceName</span></span>
<span data-ttu-id="cd3ba-122">Określa nazwę zasobu, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd3ba-122">Specifies the name of the resource that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd3ba-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd3ba-123">CommonParameters</span></span>
<span data-ttu-id="cd3ba-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd3ba-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd3ba-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd3ba-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd3ba-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cd3ba-126">INPUTS</span></span>

### <span data-ttu-id="cd3ba-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="cd3ba-127">None</span></span>

## <span data-ttu-id="cd3ba-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cd3ba-128">OUTPUTS</span></span>

### <span data-ttu-id="cd3ba-129">Interfejs IEnumerable \<ResourceCredentials\> , ResourceCredentials</span><span class="sxs-lookup"><span data-stu-id="cd3ba-129">IEnumerable\<ResourceCredentials\>, ResourceCredentials</span></span>
<span data-ttu-id="cd3ba-130">To polecenie cmdlet zwraca obiekty **ResourceCredentials** zawierające następujące właściwości:</span><span class="sxs-lookup"><span data-stu-id="cd3ba-130">This cmdlet returns **ResourceCredentials** objects that contain the following properties:</span></span> 

- <span data-ttu-id="cd3ba-131">**Source**</span><span class="sxs-lookup"><span data-stu-id="cd3ba-131">**ResourceName**</span></span>
- <span data-ttu-id="cd3ba-132">**ResouceId**</span><span class="sxs-lookup"><span data-stu-id="cd3ba-132">**ResouceId**</span></span>
- <span data-ttu-id="cd3ba-133">**ResourceState**</span><span class="sxs-lookup"><span data-stu-id="cd3ba-133">**ResourceState**</span></span>

## <span data-ttu-id="cd3ba-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cd3ba-134">NOTES</span></span>

## <span data-ttu-id="cd3ba-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cd3ba-135">RELATED LINKS</span></span>

[<span data-ttu-id="cd3ba-136">Get-AzureStorSimpleResourceContext</span><span class="sxs-lookup"><span data-stu-id="cd3ba-136">Get-AzureStorSimpleResourceContext</span></span>](./Get-AzureStorSimpleResourceContext.md)

[<span data-ttu-id="cd3ba-137">Wybierz — AzureStorSimpleResource</span><span class="sxs-lookup"><span data-stu-id="cd3ba-137">Select-AzureStorSimpleResource</span></span>](./Select-AzureStorSimpleResource.md)


