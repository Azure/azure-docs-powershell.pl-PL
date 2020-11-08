---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 03107EA1-6ADA-4A3E-B8E1-88788E5F3F37
online version: ''
schema: 2.0.0
ms.openlocfilehash: 21892d129319977897a6855933e3e8542460a4a4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055093"
---
# <span data-ttu-id="02a8a-101">Remove-AzureService</span><span class="sxs-lookup"><span data-stu-id="02a8a-101">Remove-AzureService</span></span>

## <span data-ttu-id="02a8a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="02a8a-102">SYNOPSIS</span></span>
<span data-ttu-id="02a8a-103">Usuwa bieżącą usługę w chmurze.</span><span class="sxs-lookup"><span data-stu-id="02a8a-103">Removes the current cloud service.</span></span>

## <span data-ttu-id="02a8a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="02a8a-104">SYNTAX</span></span>

```
Remove-AzureService [-ServiceName <String>] [-Force] [-PassThru] [-DeleteAll] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02a8a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="02a8a-105">DESCRIPTION</span></span>
<span data-ttu-id="02a8a-106">W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="02a8a-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="02a8a-107">Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="02a8a-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="02a8a-108">Polecenie cmdlet **Remove-AzureService** zatrzymuje, a następnie usuwa bieżącą usługę w chmurze lub usługę odpowiadającą określonej usłudze i nazwie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="02a8a-108">The **Remove-AzureService** cmdlet stops and removes the current cloud service, or the service matching the specified service and subscription name.</span></span>

## <span data-ttu-id="02a8a-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="02a8a-109">EXAMPLES</span></span>

## <span data-ttu-id="02a8a-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="02a8a-110">PARAMETERS</span></span>

### <span data-ttu-id="02a8a-111">-DeleteAll</span><span class="sxs-lookup"><span data-stu-id="02a8a-111">-DeleteAll</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02a8a-112">-Force</span><span class="sxs-lookup"><span data-stu-id="02a8a-112">-Force</span></span>
<span data-ttu-id="02a8a-113">Usuwa usługę bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="02a8a-113">Removes the service without prompting for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02a8a-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="02a8a-114">-PassThru</span></span>
<span data-ttu-id="02a8a-115">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="02a8a-115">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="02a8a-116">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="02a8a-116">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02a8a-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="02a8a-117">-Profile</span></span>
<span data-ttu-id="02a8a-118">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02a8a-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="02a8a-119">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="02a8a-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="02a8a-120">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="02a8a-120">-ServiceName</span></span>
<span data-ttu-id="02a8a-121">Określa nazwę usługi, która ma zostać usunięta.</span><span class="sxs-lookup"><span data-stu-id="02a8a-121">Specifies the name of the service to be removed.</span></span>
<span data-ttu-id="02a8a-122">Jeśli polecenie jest uruchamiane z katalogu usługi i nie określono nazwy, zostanie użyta bieżąca nazwa usługi.</span><span class="sxs-lookup"><span data-stu-id="02a8a-122">If the command is run from a service directory and no name is specified, uses the current service name.</span></span>

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

### <span data-ttu-id="02a8a-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="02a8a-123">-Confirm</span></span>
<span data-ttu-id="02a8a-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02a8a-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02a8a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02a8a-125">-WhatIf</span></span>
<span data-ttu-id="02a8a-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02a8a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02a8a-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="02a8a-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02a8a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02a8a-128">CommonParameters</span></span>
<span data-ttu-id="02a8a-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02a8a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02a8a-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02a8a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02a8a-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="02a8a-131">INPUTS</span></span>

## <span data-ttu-id="02a8a-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="02a8a-132">OUTPUTS</span></span>

## <span data-ttu-id="02a8a-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="02a8a-133">NOTES</span></span>

## <span data-ttu-id="02a8a-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="02a8a-134">RELATED LINKS</span></span>

[<span data-ttu-id="02a8a-135">Publikowanie — AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="02a8a-135">Publish-AzureServiceProject</span></span>](./Publish-AzureServiceProject.md)

[<span data-ttu-id="02a8a-136">Zatrzymaj — AzureService</span><span class="sxs-lookup"><span data-stu-id="02a8a-136">Stop-AzureService</span></span>](./Stop-AzureService.md)

[<span data-ttu-id="02a8a-137">Start — AzureService</span><span class="sxs-lookup"><span data-stu-id="02a8a-137">Start-AzureService</span></span>](./Start-AzureService.md)


