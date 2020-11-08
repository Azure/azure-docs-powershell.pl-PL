---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 756F757C-8CDE-43A5-A8A6-D55EF9C66183
online version: ''
schema: 2.0.0
ms.openlocfilehash: 71402e56251e2632c73a9185a1e70b4e3de8d770
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054967"
---
# <span data-ttu-id="923d0-101">New-AzureMediaServicesKey</span><span class="sxs-lookup"><span data-stu-id="923d0-101">New-AzureMediaServicesKey</span></span>

## <span data-ttu-id="923d0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="923d0-102">SYNOPSIS</span></span>
<span data-ttu-id="923d0-103">Umożliwia zaktualizowanie kluczy konta usługi Azure Media Services.</span><span class="sxs-lookup"><span data-stu-id="923d0-103">Updates Azure Media Services account keys.</span></span>

<span data-ttu-id="923d0-104">**Uwaga:** Ta wersja jest przestarzała, sprawdź [nowszą wersję](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).</span><span class="sxs-lookup"><span data-stu-id="923d0-104">**Note:** This version is deprecated, please see the [newer version](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).</span></span>

## <span data-ttu-id="923d0-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="923d0-105">SYNTAX</span></span>

```
New-AzureMediaServicesKey -Name <String> -KeyType <MediaServicesKeyType> [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="923d0-106">Opis</span><span class="sxs-lookup"><span data-stu-id="923d0-106">DESCRIPTION</span></span>
<span data-ttu-id="923d0-107">W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="923d0-107">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="923d0-108">Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="923d0-108">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="923d0-109">Polecenie cmdlet **New-AzureMediaServicesKey** umożliwia zaktualizowanie podstawowego lub pomocniczego klucza określonego konta usług multimedialnych.</span><span class="sxs-lookup"><span data-stu-id="923d0-109">The **New-AzureMediaServicesKey** cmdlet updates the Primary or Secondary key for the specified Media Services account.</span></span>

## <span data-ttu-id="923d0-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="923d0-110">EXAMPLES</span></span>

### <span data-ttu-id="923d0-111">Przykład 1: aktualizowanie klucza konta usług multimedialnych</span><span class="sxs-lookup"><span data-stu-id="923d0-111">Example 1: Update a Media Services account key</span></span>
```
PS C:\> New-AzureMediaServicesKey -Name "mediaservicesaccount" -KeyType "Primary" -Force
```

## <span data-ttu-id="923d0-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="923d0-112">PARAMETERS</span></span>

### <span data-ttu-id="923d0-113">-Force</span><span class="sxs-lookup"><span data-stu-id="923d0-113">-Force</span></span>
<span data-ttu-id="923d0-114">Wskazuje, że generowanie klucza nie jest potwierdzone.</span><span class="sxs-lookup"><span data-stu-id="923d0-114">Indicates that the key generation is not confirmed.</span></span>

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

### <span data-ttu-id="923d0-115">-KeyType</span><span class="sxs-lookup"><span data-stu-id="923d0-115">-KeyType</span></span>
<span data-ttu-id="923d0-116">Określa typ klucza usług multimedialnych; Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="923d0-116">Specifies the Media Services key type; Valid values are:</span></span>
  
- <span data-ttu-id="923d0-117">Początkowe</span><span class="sxs-lookup"><span data-stu-id="923d0-117">Primary</span></span>
- <span data-ttu-id="923d0-118">Dodatkowej</span><span class="sxs-lookup"><span data-stu-id="923d0-118">Secondary</span></span>

```yaml
Type: MediaServicesKeyType
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="923d0-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="923d0-119">-Name</span></span>
<span data-ttu-id="923d0-120">Określa nazwę konta usług multimedialnych.</span><span class="sxs-lookup"><span data-stu-id="923d0-120">Specifies the name of the Media Services account.</span></span>

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

### <span data-ttu-id="923d0-121">-Profile</span><span class="sxs-lookup"><span data-stu-id="923d0-121">-Profile</span></span>
<span data-ttu-id="923d0-122">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="923d0-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="923d0-123">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="923d0-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="923d0-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="923d0-124">-Confirm</span></span>
<span data-ttu-id="923d0-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="923d0-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="923d0-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="923d0-126">-WhatIf</span></span>
<span data-ttu-id="923d0-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="923d0-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="923d0-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="923d0-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="923d0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="923d0-129">CommonParameters</span></span>
<span data-ttu-id="923d0-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="923d0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="923d0-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="923d0-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="923d0-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="923d0-132">INPUTS</span></span>

## <span data-ttu-id="923d0-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="923d0-133">OUTPUTS</span></span>

## <span data-ttu-id="923d0-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="923d0-134">NOTES</span></span>

## <span data-ttu-id="923d0-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="923d0-135">RELATED LINKS</span></span>

[<span data-ttu-id="923d0-136">Jak używać usługi Azure PowerShell dla usług multimedialnych</span><span class="sxs-lookup"><span data-stu-id="923d0-136">How to use Azure PowerShell for Media Services</span></span>](https://go.microsoft.com/fwlink/?LinkId=324179)


