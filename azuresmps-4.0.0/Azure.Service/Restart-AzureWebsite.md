---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E7F6EEF0-8896-4639-89A8-810F19161211
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4b32c031a91adc3ab56e06898a1aa8ad70ac4e8d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054436"
---
# <span data-ttu-id="4dc19-101">Restart-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="4dc19-101">Restart-AzureWebsite</span></span>

## <span data-ttu-id="4dc19-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4dc19-102">SYNOPSIS</span></span>
<span data-ttu-id="4dc19-103">Zatrzymuje, a następnie ponownie uruchamia określoną witrynę sieci Web.</span><span class="sxs-lookup"><span data-stu-id="4dc19-103">Stops and then restarts the specified website.</span></span>

## <span data-ttu-id="4dc19-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4dc19-104">SYNTAX</span></span>

```
Restart-AzureWebsite [-PassThru] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="4dc19-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4dc19-105">DESCRIPTION</span></span>
<span data-ttu-id="4dc19-106">W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="4dc19-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="4dc19-107">Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="4dc19-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="4dc19-108">Polecenie cmdlet **restart-AzureWebsite** zatrzymuje, a następnie ponownie uruchamia określoną witrynę sieci Web.</span><span class="sxs-lookup"><span data-stu-id="4dc19-108">The **Restart-AzureWebsite** cmdlet stops and then restarts the specified website.</span></span>

## <span data-ttu-id="4dc19-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4dc19-109">EXAMPLES</span></span>

### <span data-ttu-id="4dc19-110">Przykład 1: ponowne uruchamianie witryny sieci Web</span><span class="sxs-lookup"><span data-stu-id="4dc19-110">Example 1: Restart a website</span></span>
```
PS C:\> Restart-AzureWebsite -Name MyWebsite
```

<span data-ttu-id="4dc19-111">W tym przykładzie zostanie ponownie uruchomiona Witryna internetowa o nazwie Moja witryna.</span><span class="sxs-lookup"><span data-stu-id="4dc19-111">This example restarts a website named MyWebsite.</span></span>

## <span data-ttu-id="4dc19-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4dc19-112">PARAMETERS</span></span>

### <span data-ttu-id="4dc19-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4dc19-113">-Name</span></span>
<span data-ttu-id="4dc19-114">Określa nazwę witryny sieci Web usługi Azure do ponownego uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="4dc19-114">Specifies the name of the Azure website to restart.</span></span>

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

### <span data-ttu-id="4dc19-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4dc19-115">-PassThru</span></span>
<span data-ttu-id="4dc19-116">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="4dc19-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4dc19-117">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="4dc19-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4dc19-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="4dc19-118">-Profile</span></span>
<span data-ttu-id="4dc19-119">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4dc19-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4dc19-120">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="4dc19-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4dc19-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="4dc19-121">-Slot</span></span>
<span data-ttu-id="4dc19-122">Określa nazwę gniazda witryny sieci Web.</span><span class="sxs-lookup"><span data-stu-id="4dc19-122">Specifies the slot name of the website.</span></span>

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

### <span data-ttu-id="4dc19-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dc19-123">CommonParameters</span></span>
<span data-ttu-id="4dc19-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4dc19-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dc19-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4dc19-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dc19-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4dc19-126">INPUTS</span></span>

## <span data-ttu-id="4dc19-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4dc19-127">OUTPUTS</span></span>

## <span data-ttu-id="4dc19-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4dc19-128">NOTES</span></span>

## <span data-ttu-id="4dc19-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4dc19-129">RELATED LINKS</span></span>

[<span data-ttu-id="4dc19-130">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="4dc19-130">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="4dc19-131">Nowe — AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="4dc19-131">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="4dc19-132">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="4dc19-132">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="4dc19-133">Start — AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="4dc19-133">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)


