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
ms.locfileid: "93887929"
---
# <span data-ttu-id="656c4-101">New-AzsIpPool</span><span class="sxs-lookup"><span data-stu-id="656c4-101">New-AzsIpPool</span></span>

## <span data-ttu-id="656c4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="656c4-102">SYNOPSIS</span></span>
<span data-ttu-id="656c4-103">Tworzenie puli adresów IP infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="656c4-103">Create an infrastructure IP pool.</span></span> <span data-ttu-id="656c4-104">Po utworzeniu puli adresów IP nie można jej usuwać ani modyfikować.</span><span class="sxs-lookup"><span data-stu-id="656c4-104">Once created an IP pool cannot be deleted or modified.</span></span>

## <span data-ttu-id="656c4-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="656c4-105">SYNTAX</span></span>

```
New-AzsIpPool [[-Name] <String>] [[-AddressPrefix] <String>] [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [[-Location] <String>] [[-ResourceGroupName] <String>]
 [[-Tags] <System.Collections.Generic.Dictionary`2[System.String,System.String]>] [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="656c4-106">Opis</span><span class="sxs-lookup"><span data-stu-id="656c4-106">DESCRIPTION</span></span>
<span data-ttu-id="656c4-107">Tworzenie puli adresów IP infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="656c4-107">Create an infrastructure IP pool.</span></span>

## <span data-ttu-id="656c4-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="656c4-108">EXAMPLES</span></span>

### <span data-ttu-id="656c4-109">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="656c4-109">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsIpPool -Name IpPool4 -StartIpAddress ***.***.***.*** -EndIpAddress ***.***.***.*** -AddressPrefix ***.***.***.***/24
```

<span data-ttu-id="656c4-110">Tworzenie nowej puli adresów IP.</span><span class="sxs-lookup"><span data-stu-id="656c4-110">Create a new IP pool.</span></span>

## <span data-ttu-id="656c4-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="656c4-111">PARAMETERS</span></span>

### <span data-ttu-id="656c4-112">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="656c4-112">-AddressPrefix</span></span>
<span data-ttu-id="656c4-113">Prefiks adresu.</span><span class="sxs-lookup"><span data-stu-id="656c4-113">The address prefix.</span></span>

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

### <span data-ttu-id="656c4-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="656c4-114">-AsJob</span></span>
<span data-ttu-id="656c4-115">Uruchamianie asynchronicznego jako zadania i zwracanie obiektu zadania.</span><span class="sxs-lookup"><span data-stu-id="656c4-115">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="656c4-116">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="656c4-116">-EndIpAddress</span></span>
<span data-ttu-id="656c4-117">Końcowy adres IP.</span><span class="sxs-lookup"><span data-stu-id="656c4-117">The ending IP address.</span></span>

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

### <span data-ttu-id="656c4-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="656c4-118">-Location</span></span>
<span data-ttu-id="656c4-119">Region, w którym znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="656c4-119">The region where the resource is located.</span></span>

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

### <span data-ttu-id="656c4-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="656c4-120">-Name</span></span>
<span data-ttu-id="656c4-121">Nazwa puli adresów IP.</span><span class="sxs-lookup"><span data-stu-id="656c4-121">IP pool name.</span></span>

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

### <span data-ttu-id="656c4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="656c4-122">-ResourceGroupName</span></span>
<span data-ttu-id="656c4-123">Grupa zasobów, w której dostawca zasobów został zarejestrowany.</span><span class="sxs-lookup"><span data-stu-id="656c4-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="656c4-124">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="656c4-124">-StartIpAddress</span></span>
<span data-ttu-id="656c4-125">Początkowy adres IP.</span><span class="sxs-lookup"><span data-stu-id="656c4-125">The starting IP address.</span></span>

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

### <span data-ttu-id="656c4-126">-Tagi</span><span class="sxs-lookup"><span data-stu-id="656c4-126">-Tags</span></span>
<span data-ttu-id="656c4-127">Lista par klucz-wartość.</span><span class="sxs-lookup"><span data-stu-id="656c4-127">List of key-value pairs.</span></span>

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

### <span data-ttu-id="656c4-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="656c4-128">-Confirm</span></span>
<span data-ttu-id="656c4-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="656c4-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="656c4-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="656c4-130">-WhatIf</span></span>
<span data-ttu-id="656c4-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="656c4-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="656c4-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="656c4-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="656c4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="656c4-133">CommonParameters</span></span>
<span data-ttu-id="656c4-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="656c4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="656c4-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="656c4-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="656c4-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="656c4-136">INPUTS</span></span>

## <span data-ttu-id="656c4-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="656c4-137">OUTPUTS</span></span>

### <span data-ttu-id="656c4-138">Microsoft. AzureStack. Management. Fabric. admin. models. ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="656c4-138">Microsoft.AzureStack.Management.Fabric.Admin.Models.ProvisioningState</span></span>

## <span data-ttu-id="656c4-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="656c4-139">NOTES</span></span>

## <span data-ttu-id="656c4-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="656c4-140">RELATED LINKS</span></span>

