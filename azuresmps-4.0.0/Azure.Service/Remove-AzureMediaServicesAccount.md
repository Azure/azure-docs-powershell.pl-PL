---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 5B255D11-0A9B-4679-A2AC-4357B293EE96
online version: ''
schema: 2.0.0
ms.openlocfilehash: e4eee130312ae52e95b020151750d46144bc3685
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055437"
---
# <span data-ttu-id="14576-101">Remove-AzureMediaServicesAccount</span><span class="sxs-lookup"><span data-stu-id="14576-101">Remove-AzureMediaServicesAccount</span></span>

## <span data-ttu-id="14576-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="14576-102">SYNOPSIS</span></span>
<span data-ttu-id="14576-103">Usuwa określone konto usługi Azure Media Services.</span><span class="sxs-lookup"><span data-stu-id="14576-103">Removes the specified Azure Media Services account.</span></span>

<span data-ttu-id="14576-104">**Uwaga:**  Ta wersja jest przestarzała, sprawdź [nowszą wersję](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).</span><span class="sxs-lookup"><span data-stu-id="14576-104">**Note:**  This version is deprecated, please see the [newer version](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).</span></span>

## <span data-ttu-id="14576-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="14576-105">SYNTAX</span></span>

```
Remove-AzureMediaServicesAccount -Name <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="14576-106">Opis</span><span class="sxs-lookup"><span data-stu-id="14576-106">DESCRIPTION</span></span>
<span data-ttu-id="14576-107">W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="14576-107">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="14576-108">Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="14576-108">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="14576-109">Polecenie cmdlet **Remove-AzureMediaServicesAccount** usuwa konto usług multimedialnych.</span><span class="sxs-lookup"><span data-stu-id="14576-109">The **Remove-AzureMediaServicesAccount** cmdlet removes a Media Services account.</span></span>

## <span data-ttu-id="14576-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="14576-110">EXAMPLES</span></span>

### <span data-ttu-id="14576-111">Przykład 1: usuwanie konta usług multimedialnych</span><span class="sxs-lookup"><span data-stu-id="14576-111">Example 1: Delete a Media Services account</span></span>
```
PS C:\> Remove-AzureMediaServicesAccount -Name "mediaservicesaccount" -Force
```

## <span data-ttu-id="14576-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="14576-112">PARAMETERS</span></span>

### <span data-ttu-id="14576-113">-Force</span><span class="sxs-lookup"><span data-stu-id="14576-113">-Force</span></span>
<span data-ttu-id="14576-114">Jeśli jest określony przełącznik *Force* , usunięcie nie jest potwierdzone.</span><span class="sxs-lookup"><span data-stu-id="14576-114">If the *Force* switch is specified, the deletion is not confirmed.</span></span>

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

### <span data-ttu-id="14576-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="14576-115">-Name</span></span>
<span data-ttu-id="14576-116">Nazwa konta usług multimedialnych.</span><span class="sxs-lookup"><span data-stu-id="14576-116">The Media Services account name.</span></span>

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

### <span data-ttu-id="14576-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="14576-117">-Profile</span></span>
<span data-ttu-id="14576-118">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14576-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="14576-119">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="14576-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="14576-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="14576-120">-Confirm</span></span>
<span data-ttu-id="14576-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14576-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14576-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14576-122">-WhatIf</span></span>
<span data-ttu-id="14576-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14576-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14576-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="14576-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14576-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14576-125">CommonParameters</span></span>
<span data-ttu-id="14576-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14576-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14576-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14576-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14576-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="14576-128">INPUTS</span></span>

## <span data-ttu-id="14576-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="14576-129">OUTPUTS</span></span>

## <span data-ttu-id="14576-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="14576-130">NOTES</span></span>

## <span data-ttu-id="14576-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="14576-131">RELATED LINKS</span></span>

[<span data-ttu-id="14576-132">Jak używać usługi Azure PowerShell dla usług multimedialnych</span><span class="sxs-lookup"><span data-stu-id="14576-132">How to use Azure PowerShell for Media Services</span></span>](https://go.microsoft.com/fwlink/?LinkId=324179)

[<span data-ttu-id="14576-133">Get-AzureMediaServicesAccount</span><span class="sxs-lookup"><span data-stu-id="14576-133">Get-AzureMediaServicesAccount</span></span>](./Get-AzureMediaServicesAccount.md)

[<span data-ttu-id="14576-134">Nowe — AzureMediaServicesAccount</span><span class="sxs-lookup"><span data-stu-id="14576-134">New-AzureMediaServicesAccount</span></span>](./New-AzureMediaServicesAccount.md)


