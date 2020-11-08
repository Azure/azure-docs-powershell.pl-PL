---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: E771D1F2-A06B-44BB-AAFF-9459DC6303E6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 273edfe08e4d2476cd4c1baa2967a829ec1bbcc2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054414"
---
# <span data-ttu-id="ba53f-101">Select-AzureStorSimpleResource</span><span class="sxs-lookup"><span data-stu-id="ba53f-101">Select-AzureStorSimpleResource</span></span>

## <span data-ttu-id="ba53f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ba53f-102">SYNOPSIS</span></span>
<span data-ttu-id="ba53f-103">Ustawia zasób jako bieżący zasób.</span><span class="sxs-lookup"><span data-stu-id="ba53f-103">Sets a resource as the current resource.</span></span>

## <span data-ttu-id="ba53f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ba53f-104">SYNTAX</span></span>

```
Select-AzureStorSimpleResource -ResourceName <String> [-RegistrationKey <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="ba53f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ba53f-105">DESCRIPTION</span></span>
<span data-ttu-id="ba53f-106">Polecenie cmdlet **SELECT-AzureStorSimpleResource** ustawia zasób jako bieżący zasób.</span><span class="sxs-lookup"><span data-stu-id="ba53f-106">The **Select-AzureStorSimpleResource** cmdlet sets a resource as the current resource.</span></span>
<span data-ttu-id="ba53f-107">Po wybraniu zasobu inne polecenia cmdlet będą stosowane w tym kontekście zasobów.</span><span class="sxs-lookup"><span data-stu-id="ba53f-107">After you select a resource, other cmdlets apply within that resource context.</span></span>

## <span data-ttu-id="ba53f-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ba53f-108">EXAMPLES</span></span>

### <span data-ttu-id="ba53f-109">Przykład 1. Wybieranie zasobu po raz pierwszy</span><span class="sxs-lookup"><span data-stu-id="ba53f-109">Example 1: Select a resource for the first time</span></span>
```
PS C:\>Select-AzureStorSimpleResource -ResourceName "Contoso64-Tsqa" -RegistrationKey "<your registration key>"
ResourceId           ResourceName
----------           ------------
1909806764156522689  Contoso64-Tsqa
```

<span data-ttu-id="ba53f-110">To polecenie umożliwia wybranie zasobu o nazwie Contoso64-Tsqa jako bieżącego kontekstu.</span><span class="sxs-lookup"><span data-stu-id="ba53f-110">This command selects the resource named Contoso64-Tsqa as the current context.</span></span>
<span data-ttu-id="ba53f-111">W tym przykładzie nie zainicjowano wcześniej tego kontekstu na komputerze, dlatego należy określić wartość parametru *RegistrationKey* .</span><span class="sxs-lookup"><span data-stu-id="ba53f-111">In this example, the computer has not had this context initialized previously, and, therefore, you must specify a value for the *RegistrationKey* parameter.</span></span>

### <span data-ttu-id="ba53f-112">Przykład 2: próba wybrania zasobu</span><span class="sxs-lookup"><span data-stu-id="ba53f-112">Example 2: Attempt to select a resource</span></span>
```
This command gets the current context for this computer by using the **Get-AzureStorSimpleResourceContext** cmdlet. The current selected resource is Contoso64-Tsqa. This is consistent with the previous example. 
PS C:\>Get-AzureStorSimpleResourceContext
ResourceId           ResourceName
----------           ------------
1909806764156522689  Contoso64-Tsqa 

This command attempts to reset the resource to be Contoso02-Resource. For this example, this resource has not been previously selected. The registration key is not saved or included in the command. The command cannot select the resource. 
PS C:\>Select-AzureStorSimpleResource -ResourceName "Contoso02-Resource"
Select-AzureStorSimpleResource : Could not find the persisted secret. Please use Select-AzureStorSimpleResource and
provide the Registration key once again.
```

### <span data-ttu-id="ba53f-113">Przykład 3: Zaznaczanie uprzednio wybranego zasobu</span><span class="sxs-lookup"><span data-stu-id="ba53f-113">Example 3: Select a previously selected resource</span></span>
```
PS C:\>Select-AzureStorSimpleResource -ResourceName "Contoso64-Tsqa"
ResourceId           ResourceName
----------           ------------
1909806764156522689  Contoso64-Tsqa
```

<span data-ttu-id="ba53f-114">To polecenie umożliwia wybranie zasobu o nazwie Contoso64-Tsqa jako bieżącego kontekstu.</span><span class="sxs-lookup"><span data-stu-id="ba53f-114">This command selects the resource named Contoso64-Tsqa as the current context.</span></span>
<span data-ttu-id="ba53f-115">W tym przykładzie kontekst został już wybrany, a więc nie musisz określać wartości parametru *RegistrationKey* .</span><span class="sxs-lookup"><span data-stu-id="ba53f-115">In this example, that context has previously been selected, and, therefore, you do not need to specify a value for the *RegistrationKey* parameter.</span></span>

## <span data-ttu-id="ba53f-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ba53f-116">PARAMETERS</span></span>

### <span data-ttu-id="ba53f-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="ba53f-117">-Profile</span></span>
<span data-ttu-id="ba53f-118">Określa Profil platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ba53f-118">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="ba53f-119">-RegistrationKey</span><span class="sxs-lookup"><span data-stu-id="ba53f-119">-RegistrationKey</span></span>
<span data-ttu-id="ba53f-120">Określa klucz rejestracji.</span><span class="sxs-lookup"><span data-stu-id="ba53f-120">Specifies a registration key.</span></span>
<span data-ttu-id="ba53f-121">Określ klucz przy pierwszym wybraniu zasobu.</span><span class="sxs-lookup"><span data-stu-id="ba53f-121">Specify a key the first time that you select a resource.</span></span>
<span data-ttu-id="ba53f-122">Gdy to polecenie cmdlet wybierzesz bieżący zasób, polecenia cmdlet użyją tego klucza stosownie do potrzeb.</span><span class="sxs-lookup"><span data-stu-id="ba53f-122">After this cmdlet selects the current resource, cmdlets use this key, as required.</span></span>
<span data-ttu-id="ba53f-123">Aby uzyskać więcej informacji, zobacz [Uzyskiwanie klucza rejestracji usługi](https://msdn.microsoft.com/en-us/library/azure/dn772346.aspx)  ( https://msdn.microsoft.com/en-us/library/azure/dn772346.aspx) w witrynie Microsoft Developer Network.</span><span class="sxs-lookup"><span data-stu-id="ba53f-123">For more information, see [Get the service registration key](https://msdn.microsoft.com/en-us/library/azure/dn772346.aspx)  (https://msdn.microsoft.com/en-us/library/azure/dn772346.aspx) on the Microsoft Developer Network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba53f-124">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="ba53f-124">-ResourceName</span></span>
<span data-ttu-id="ba53f-125">Określa nazwę zasobu, który ma zostać wybrany jako bieżący zasób.</span><span class="sxs-lookup"><span data-stu-id="ba53f-125">Specifies the name of the resource to select as the current resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba53f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba53f-126">CommonParameters</span></span>
<span data-ttu-id="ba53f-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba53f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba53f-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba53f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba53f-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ba53f-129">INPUTS</span></span>

### <span data-ttu-id="ba53f-130">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="ba53f-130">None</span></span>

## <span data-ttu-id="ba53f-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ba53f-131">OUTPUTS</span></span>

### <span data-ttu-id="ba53f-132">StorSimpleResourceContext</span><span class="sxs-lookup"><span data-stu-id="ba53f-132">StorSimpleResourceContext</span></span>
<span data-ttu-id="ba53f-133">To polecenie cmdlet zwraca obiekt **StorSimpleResourceContext** , który zawiera szczegółowe informacje dotyczące kontekstu zasobów.</span><span class="sxs-lookup"><span data-stu-id="ba53f-133">This cmdlet returns a **StorSimpleResourceContext** object that contains details for the resource context.</span></span>

## <span data-ttu-id="ba53f-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ba53f-134">NOTES</span></span>

## <span data-ttu-id="ba53f-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ba53f-135">RELATED LINKS</span></span>

[<span data-ttu-id="ba53f-136">Get-AzureStorSimpleResource</span><span class="sxs-lookup"><span data-stu-id="ba53f-136">Get-AzureStorSimpleResource</span></span>](./Get-AzureStorSimpleResource.md)

[<span data-ttu-id="ba53f-137">Get-AzureStorSimpleResourceContext</span><span class="sxs-lookup"><span data-stu-id="ba53f-137">Get-AzureStorSimpleResourceContext</span></span>](./Get-AzureStorSimpleResourceContext.md)


