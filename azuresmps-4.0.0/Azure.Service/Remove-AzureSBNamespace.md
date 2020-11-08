---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 6E369BDF-AE3C-416B-81B7-097C20147CBE
online version: ''
schema: 2.0.0
ms.openlocfilehash: bb48f7412c957ceefb7df03d79e57ce8e75447d5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055096"
---
# <span data-ttu-id="b6c5f-101">Remove-AzureSBNamespace</span><span class="sxs-lookup"><span data-stu-id="b6c5f-101">Remove-AzureSBNamespace</span></span>

## <span data-ttu-id="b6c5f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b6c5f-102">SYNOPSIS</span></span>
<span data-ttu-id="b6c5f-103">Usuwa obszar nazw.</span><span class="sxs-lookup"><span data-stu-id="b6c5f-103">Removes a namespace.</span></span>

## <span data-ttu-id="b6c5f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b6c5f-104">SYNTAX</span></span>

```
Remove-AzureSBNamespace -Name <String> [-PassThru] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b6c5f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b6c5f-105">DESCRIPTION</span></span>
<span data-ttu-id="b6c5f-106">W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b6c5f-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="b6c5f-107">Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="b6c5f-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="b6c5f-108">Polecenie cmdlet **Remove-AzureSBNamespace** usuwa obszar nazw usługi dla magistrali usług.</span><span class="sxs-lookup"><span data-stu-id="b6c5f-108">The **Remove-AzureSBNamespace** cmdlet removes a service namespace for Service Bus.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="b6c5f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b6c5f-109">EXAMPLES</span></span>

## <span data-ttu-id="b6c5f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b6c5f-110">PARAMETERS</span></span>

### <span data-ttu-id="b6c5f-111">-Force</span><span class="sxs-lookup"><span data-stu-id="b6c5f-111">-Force</span></span>
<span data-ttu-id="b6c5f-112">Jeśli ta opcja jest włączona, obszar nazw jest usuwany bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b6c5f-112">If enabled, removes the namespace without prompting for confirmation.</span></span>

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

### <span data-ttu-id="b6c5f-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b6c5f-113">-Name</span></span>
<span data-ttu-id="b6c5f-114">Określa nazwę obszaru nazw, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="b6c5f-114">Specifies the name of the namespace to be removed.</span></span>

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

### <span data-ttu-id="b6c5f-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b6c5f-115">-PassThru</span></span>
<span data-ttu-id="b6c5f-116">Powoduje, że operacja zwraca wartość PRAWDA, jeśli to się powiedzie.</span><span class="sxs-lookup"><span data-stu-id="b6c5f-116">Causes the operation to return true if it succeeds.</span></span>

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

### <span data-ttu-id="b6c5f-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="b6c5f-117">-Profile</span></span>
<span data-ttu-id="b6c5f-118">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6c5f-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b6c5f-119">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="b6c5f-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b6c5f-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b6c5f-120">-Confirm</span></span>
<span data-ttu-id="b6c5f-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6c5f-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6c5f-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6c5f-122">-WhatIf</span></span>
<span data-ttu-id="b6c5f-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6c5f-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6c5f-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b6c5f-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6c5f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6c5f-125">CommonParameters</span></span>
<span data-ttu-id="b6c5f-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6c5f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6c5f-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6c5f-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6c5f-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b6c5f-128">INPUTS</span></span>

## <span data-ttu-id="b6c5f-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b6c5f-129">OUTPUTS</span></span>

## <span data-ttu-id="b6c5f-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b6c5f-130">NOTES</span></span>

## <span data-ttu-id="b6c5f-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b6c5f-131">RELATED LINKS</span></span>

[<span data-ttu-id="b6c5f-132">Nowe — AzureSBNamespace</span><span class="sxs-lookup"><span data-stu-id="b6c5f-132">New-AzureSBNamespace</span></span>](./New-AzureSBNamespace.md)


