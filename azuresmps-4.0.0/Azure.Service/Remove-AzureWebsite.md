---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 8062D57E-8381-4715-9AA8-551F15DCC492
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2627bdb2f098d5b09851ec5970dd2a73840d24e6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054449"
---
# <span data-ttu-id="6f26a-101">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="6f26a-101">Remove-AzureWebsite</span></span>

## <span data-ttu-id="6f26a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6f26a-102">SYNOPSIS</span></span>
<span data-ttu-id="6f26a-103">Usuwa określoną witrynę sieci Web z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6f26a-103">Removes the specified website from Azure.</span></span>

## <span data-ttu-id="6f26a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6f26a-104">SYNTAX</span></span>

```
Remove-AzureWebsite [-Force] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6f26a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6f26a-105">DESCRIPTION</span></span>
<span data-ttu-id="6f26a-106">W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6f26a-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="6f26a-107">Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="6f26a-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="6f26a-108">Polecenie cmdlet **Remove-AzureWebsite** usuwa określoną witrynę sieci Web z usługi Azure z monitem o potwierdzenie lub bez niego.</span><span class="sxs-lookup"><span data-stu-id="6f26a-108">The **Remove-AzureWebsite** cmdlet removes the specified website from Azure, either with or without a prompt for confirmation.</span></span>

## <span data-ttu-id="6f26a-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6f26a-109">EXAMPLES</span></span>

### <span data-ttu-id="6f26a-110">Przykład 1: usuwanie bieżącej witryny sieci Web</span><span class="sxs-lookup"><span data-stu-id="6f26a-110">Example 1: Remove the current website</span></span>
```
PS C:\> Remove-AzureWebsite
```

<span data-ttu-id="6f26a-111">W tym przykładzie usunięto witrynę sieci Web w usłudze Azure skojarzoną z bieżącym katalogiem.</span><span class="sxs-lookup"><span data-stu-id="6f26a-111">This example removes the website in Azure associated with the current directory.</span></span>

### <span data-ttu-id="6f26a-112">Przykład 2: usuwanie witryny sieci Web bez potwierdzenia</span><span class="sxs-lookup"><span data-stu-id="6f26a-112">Example 2: Remove a website without confirmation</span></span>
```
PS C:\> Remove-AzureWebsite -Name mySite -Force
```

<span data-ttu-id="6f26a-113">W tym przykładzie zostanie usunięta witryna sieci Web o nazwie Moja witryna bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6f26a-113">This example deletes the website named mySite without prompting for confirmation.</span></span>

## <span data-ttu-id="6f26a-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6f26a-114">PARAMETERS</span></span>

### <span data-ttu-id="6f26a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="6f26a-115">-Force</span></span>
<span data-ttu-id="6f26a-116">Jeśli ta opcja jest określona, usuwa określoną witrynę sieci Web bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6f26a-116">If specified, deletes the specified website without prompting for confirmation.</span></span>

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

### <span data-ttu-id="6f26a-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6f26a-117">-Name</span></span>
<span data-ttu-id="6f26a-118">Określa nazwę witryny sieci Web, którą należy usunąć.</span><span class="sxs-lookup"><span data-stu-id="6f26a-118">Specifies the name of the website to delete.</span></span>

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

### <span data-ttu-id="6f26a-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="6f26a-119">-Profile</span></span>
<span data-ttu-id="6f26a-120">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6f26a-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6f26a-121">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="6f26a-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6f26a-122">-Slot</span><span class="sxs-lookup"><span data-stu-id="6f26a-122">-Slot</span></span>
<span data-ttu-id="6f26a-123">Określa nazwę gniazda witryny sieci Web.</span><span class="sxs-lookup"><span data-stu-id="6f26a-123">Specifies the slot name of the website.</span></span>

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

### <span data-ttu-id="6f26a-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6f26a-124">-Confirm</span></span>
<span data-ttu-id="6f26a-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6f26a-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f26a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f26a-126">-WhatIf</span></span>
<span data-ttu-id="6f26a-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6f26a-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f26a-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6f26a-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f26a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f26a-129">CommonParameters</span></span>
<span data-ttu-id="6f26a-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f26a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f26a-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f26a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f26a-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6f26a-132">INPUTS</span></span>

## <span data-ttu-id="6f26a-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6f26a-133">OUTPUTS</span></span>

## <span data-ttu-id="6f26a-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6f26a-134">NOTES</span></span>

## <span data-ttu-id="6f26a-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6f26a-135">RELATED LINKS</span></span>

[<span data-ttu-id="6f26a-136">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="6f26a-136">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)


