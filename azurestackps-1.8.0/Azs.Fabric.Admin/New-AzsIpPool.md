---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: bd353b28b095178e83f488f3fd05a54146610b01
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2020
ms.locfileid: "93888934"
---
# <span data-ttu-id="066d0-101">New-AzsIpPool</span><span class="sxs-lookup"><span data-stu-id="066d0-101">New-AzsIpPool</span></span>

## <span data-ttu-id="066d0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="066d0-102">SYNOPSIS</span></span>
<span data-ttu-id="066d0-103">Tworzenie puli adresów IP infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="066d0-103">Create an infrastructure IP pool.</span></span> <span data-ttu-id="066d0-104">Po utworzeniu puli adresów IP nie można jej usuwać ani modyfikować.</span><span class="sxs-lookup"><span data-stu-id="066d0-104">Once created an IP pool cannot be deleted or modified.</span></span>

## <span data-ttu-id="066d0-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="066d0-105">SYNTAX</span></span>

```
New-AzsIpPool [[-Name] <String>] [[-AddressPrefix] <String>] [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [[-Location] <String>] [[-ResourceGroupName] <String>]
 [[-Tags] <System.Collections.Generic.Dictionary`2[System.String,System.String]>] [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="066d0-106">Opis</span><span class="sxs-lookup"><span data-stu-id="066d0-106">DESCRIPTION</span></span>
<span data-ttu-id="066d0-107">Tworzenie puli adresów IP infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="066d0-107">Create an infrastructure IP pool.</span></span>

## <span data-ttu-id="066d0-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="066d0-108">EXAMPLES</span></span>

### <span data-ttu-id="066d0-109">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="066d0-109">EXAMPLE 1</span></span>
```
New-AzsIpPool -Name IpPool4 -StartIpAddress ***.***.***.*** -EndIpAddress ***.***.***.*** -AddressPrefix ***.***.***.***/24
```

<span data-ttu-id="066d0-110">Tworzenie nowej puli adresów IP.</span><span class="sxs-lookup"><span data-stu-id="066d0-110">Create a new IP pool.</span></span>

## <span data-ttu-id="066d0-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="066d0-111">PARAMETERS</span></span>

### <span data-ttu-id="066d0-112">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="066d0-112">-Name</span></span>
<span data-ttu-id="066d0-113">Nazwa puli adresów IP.</span><span class="sxs-lookup"><span data-stu-id="066d0-113">IP pool name.</span></span>

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

### <span data-ttu-id="066d0-114">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="066d0-114">-AddressPrefix</span></span>
<span data-ttu-id="066d0-115">Prefiks adresu.</span><span class="sxs-lookup"><span data-stu-id="066d0-115">The address prefix.</span></span>

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

### <span data-ttu-id="066d0-116">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="066d0-116">-StartIpAddress</span></span>
<span data-ttu-id="066d0-117">Początkowy adres IP.</span><span class="sxs-lookup"><span data-stu-id="066d0-117">The starting IP address.</span></span>

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

### <span data-ttu-id="066d0-118">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="066d0-118">-EndIpAddress</span></span>
<span data-ttu-id="066d0-119">Końcowy adres IP.</span><span class="sxs-lookup"><span data-stu-id="066d0-119">The ending IP address.</span></span>

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

### <span data-ttu-id="066d0-120">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="066d0-120">-Location</span></span>
<span data-ttu-id="066d0-121">Region, w którym znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="066d0-121">The region where the resource is located.</span></span>

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

### <span data-ttu-id="066d0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="066d0-122">-ResourceGroupName</span></span>
<span data-ttu-id="066d0-123">Grupa zasobów, w której dostawca zasobów został zarejestrowany.</span><span class="sxs-lookup"><span data-stu-id="066d0-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="066d0-124">-Tagi</span><span class="sxs-lookup"><span data-stu-id="066d0-124">-Tags</span></span>
<span data-ttu-id="066d0-125">Lista par klucz-wartość.</span><span class="sxs-lookup"><span data-stu-id="066d0-125">List of key-value pairs.</span></span>

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

### <span data-ttu-id="066d0-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="066d0-126">-AsJob</span></span>
<span data-ttu-id="066d0-127">Uruchamianie asynchronicznego jako zadania i zwracanie obiektu zadania.</span><span class="sxs-lookup"><span data-stu-id="066d0-127">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="066d0-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="066d0-128">-WhatIf</span></span>
<span data-ttu-id="066d0-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="066d0-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="066d0-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="066d0-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="066d0-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="066d0-131">-Confirm</span></span>
<span data-ttu-id="066d0-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="066d0-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="066d0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="066d0-133">CommonParameters</span></span>
<span data-ttu-id="066d0-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="066d0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="066d0-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="066d0-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="066d0-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="066d0-136">INPUTS</span></span>

## <span data-ttu-id="066d0-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="066d0-137">OUTPUTS</span></span>

### <span data-ttu-id="066d0-138">Microsoft. AzureStack. Management. Fabric. admin. models. ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="066d0-138">Microsoft.AzureStack.Management.Fabric.Admin.Models.ProvisioningState</span></span>

## <span data-ttu-id="066d0-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="066d0-139">NOTES</span></span>

## <span data-ttu-id="066d0-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="066d0-140">RELATED LINKS</span></span>
