---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b50cd7f98fd9919ed816314d7cec1222e5c4970c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523190"
---
# <span data-ttu-id="b1177-101">New-AzsIpPool</span><span class="sxs-lookup"><span data-stu-id="b1177-101">New-AzsIpPool</span></span>

## <span data-ttu-id="b1177-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b1177-102">SYNOPSIS</span></span>
<span data-ttu-id="b1177-103">Tworzenie puli adresów IP infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="b1177-103">Create an infrastructure IP pool.</span></span> <span data-ttu-id="b1177-104">Po utworzeniu puli adresów IP nie można jej usuwać ani modyfikować.</span><span class="sxs-lookup"><span data-stu-id="b1177-104">Once created an IP pool cannot be deleted or modified.</span></span>

## <span data-ttu-id="b1177-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b1177-105">SYNTAX</span></span>

```
New-AzsIpPool [[-Name] <String>] [[-AddressPrefix] <String>] [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [[-Location] <String>] [[-ResourceGroupName] <String>]
 [[-Tags] <System.Collections.Generic.Dictionary`2[System.String,System.String]>] [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b1177-106">Opis</span><span class="sxs-lookup"><span data-stu-id="b1177-106">DESCRIPTION</span></span>
<span data-ttu-id="b1177-107">Tworzenie puli adresów IP infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="b1177-107">Create an infrastructure IP pool.</span></span>

## <span data-ttu-id="b1177-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b1177-108">EXAMPLES</span></span>

### <span data-ttu-id="b1177-109">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b1177-109">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsIpPool -Name IpPool4 -StartIpAddress ***.***.***.*** -EndIpAddress ***.***.***.*** -AddressPrefix ***.***.***.***/24
```

<span data-ttu-id="b1177-110">Tworzenie nowej puli adresów IP.</span><span class="sxs-lookup"><span data-stu-id="b1177-110">Create a new IP pool.</span></span>

## <span data-ttu-id="b1177-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b1177-111">PARAMETERS</span></span>

### <span data-ttu-id="b1177-112">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="b1177-112">-AddressPrefix</span></span>
<span data-ttu-id="b1177-113">Prefiks adresu.</span><span class="sxs-lookup"><span data-stu-id="b1177-113">The address prefix.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1177-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b1177-114">-AsJob</span></span>
<span data-ttu-id="b1177-115">Uruchamianie asynchronicznego jako zadania i zwracanie obiektu zadania.</span><span class="sxs-lookup"><span data-stu-id="b1177-115">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1177-116">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="b1177-116">-EndIpAddress</span></span>
<span data-ttu-id="b1177-117">Końcowy adres IP.</span><span class="sxs-lookup"><span data-stu-id="b1177-117">The ending IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1177-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="b1177-118">-Location</span></span>
<span data-ttu-id="b1177-119">Region, w którym znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="b1177-119">The region where the resource is located.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1177-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b1177-120">-Name</span></span>
<span data-ttu-id="b1177-121">Nazwa puli adresów IP.</span><span class="sxs-lookup"><span data-stu-id="b1177-121">IP pool name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1177-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1177-122">-ResourceGroupName</span></span>
<span data-ttu-id="b1177-123">Grupa zasobów, w której dostawca zasobów został zarejestrowany.</span><span class="sxs-lookup"><span data-stu-id="b1177-123">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1177-124">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="b1177-124">-StartIpAddress</span></span>
<span data-ttu-id="b1177-125">Początkowy adres IP.</span><span class="sxs-lookup"><span data-stu-id="b1177-125">The starting IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1177-126">-Tagi</span><span class="sxs-lookup"><span data-stu-id="b1177-126">-Tags</span></span>
<span data-ttu-id="b1177-127">Lista par klucz-wartość.</span><span class="sxs-lookup"><span data-stu-id="b1177-127">List of key-value pairs.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1177-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b1177-128">-Confirm</span></span>
<span data-ttu-id="b1177-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1177-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1177-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1177-130">-WhatIf</span></span>
<span data-ttu-id="b1177-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1177-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1177-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b1177-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1177-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1177-133">CommonParameters</span></span>
<span data-ttu-id="b1177-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1177-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1177-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1177-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1177-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b1177-136">INPUTS</span></span>

## <span data-ttu-id="b1177-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b1177-137">OUTPUTS</span></span>

### <span data-ttu-id="b1177-138">Microsoft. AzureStack. Management. Fabric. admin. models. ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="b1177-138">Microsoft.AzureStack.Management.Fabric.Admin.Models.ProvisioningState</span></span>

## <span data-ttu-id="b1177-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b1177-139">NOTES</span></span>

## <span data-ttu-id="b1177-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b1177-140">RELATED LINKS</span></span>

