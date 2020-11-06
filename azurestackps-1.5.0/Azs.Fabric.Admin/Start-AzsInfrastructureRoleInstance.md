---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: f5a52ebfe2d59a200add1c8f763f7a3cafa59c18
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523965"
---
# <span data-ttu-id="a1cd1-101">Start-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="a1cd1-101">Start-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="a1cd1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a1cd1-102">SYNOPSIS</span></span>
<span data-ttu-id="a1cd1-103">Włączanie wystąpienia roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="a1cd1-103">Power on an infrastructure role instance.</span></span>

## <span data-ttu-id="a1cd1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a1cd1-104">SYNTAX</span></span>

### <span data-ttu-id="a1cd1-105">PowerOn (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a1cd1-105">PowerOn (Default)</span></span>
```
Start-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1cd1-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="a1cd1-106">ResourceId</span></span>
```
Start-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a1cd1-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a1cd1-107">DESCRIPTION</span></span>
<span data-ttu-id="a1cd1-108">Włączanie wystąpienia roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="a1cd1-108">Power on an infrastructure role instance.</span></span>

## <span data-ttu-id="a1cd1-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a1cd1-109">EXAMPLES</span></span>

### <span data-ttu-id="a1cd1-110">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="a1cd1-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Start-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="a1cd1-111">Włączanie wystąpienia roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="a1cd1-111">Power on an infrastructure role instance.</span></span>

## <span data-ttu-id="a1cd1-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a1cd1-112">PARAMETERS</span></span>

### <span data-ttu-id="a1cd1-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a1cd1-113">-AsJob</span></span>
<span data-ttu-id="a1cd1-114">Uruchamianie asynchronicznego jako zadania i zwracanie obiektu zadania.</span><span class="sxs-lookup"><span data-stu-id="a1cd1-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="a1cd1-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a1cd1-115">-Force</span></span>
<span data-ttu-id="a1cd1-116">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a1cd1-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="a1cd1-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="a1cd1-117">-Location</span></span>
<span data-ttu-id="a1cd1-118">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="a1cd1-118">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: PowerOn
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1cd1-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a1cd1-119">-Name</span></span>
<span data-ttu-id="a1cd1-120">Nazwa wystąpienia roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="a1cd1-120">Name of an infrastructure role instance.</span></span>

```yaml
Type: String
Parameter Sets: PowerOn
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1cd1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1cd1-121">-ResourceGroupName</span></span>
<span data-ttu-id="a1cd1-122">Grupa zasobów, w której dostawca zasobów został zarejestrowany.</span><span class="sxs-lookup"><span data-stu-id="a1cd1-122">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: PowerOn
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1cd1-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a1cd1-123">-ResourceId</span></span>
<span data-ttu-id="a1cd1-124">Identyfikator zasobu wystąpienia roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="a1cd1-124">Infrastructure role instance resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1cd1-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a1cd1-125">-Confirm</span></span>
<span data-ttu-id="a1cd1-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1cd1-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1cd1-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1cd1-127">-WhatIf</span></span>
<span data-ttu-id="a1cd1-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1cd1-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1cd1-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a1cd1-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1cd1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1cd1-130">CommonParameters</span></span>
<span data-ttu-id="a1cd1-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1cd1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1cd1-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1cd1-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1cd1-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a1cd1-133">INPUTS</span></span>

## <span data-ttu-id="a1cd1-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a1cd1-134">OUTPUTS</span></span>

## <span data-ttu-id="a1cd1-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a1cd1-135">NOTES</span></span>

## <span data-ttu-id="a1cd1-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a1cd1-136">RELATED LINKS</span></span>

