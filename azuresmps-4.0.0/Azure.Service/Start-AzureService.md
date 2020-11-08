---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 821CB3E4-102E-440A-8C92-D1890899A6EE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 64924d579eebb826bc9c36468da1617370f48cf7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054996"
---
# <span data-ttu-id="e3d35-101">Start-AzureService</span><span class="sxs-lookup"><span data-stu-id="e3d35-101">Start-AzureService</span></span>

## <span data-ttu-id="e3d35-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e3d35-102">SYNOPSIS</span></span>
<span data-ttu-id="e3d35-103">Rozpoczyna określoną hostowaną usługę w systemie Windows Azure.</span><span class="sxs-lookup"><span data-stu-id="e3d35-103">Starts the specified hosted service in Windows Azure.</span></span>

## <span data-ttu-id="e3d35-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e3d35-104">SYNTAX</span></span>

```
Start-AzureService [-ServiceName <String>] [-Slot <String>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="e3d35-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e3d35-105">DESCRIPTION</span></span>
<span data-ttu-id="e3d35-106">W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e3d35-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="e3d35-107">Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="e3d35-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="e3d35-108">Polecenie cmdlet **Start-AzureService** uruchamia określoną usługę hostowaną na platformie Windows Azure, jeśli usługa jest w stanie zatrzymania.</span><span class="sxs-lookup"><span data-stu-id="e3d35-108">The **Start-AzureService** cmdlet starts the specified hosted service in Windows Azure, if the service is in the stopped state.</span></span>
<span data-ttu-id="e3d35-109">Należy zauważyć, że polecenie cmdlet **Publish-AzureServiceProject** automatycznie próbuje uruchomić usługę.</span><span class="sxs-lookup"><span data-stu-id="e3d35-109">Note that the **Publish-AzureServiceProject** cmdlet automatically attempts to start the service.</span></span>

## <span data-ttu-id="e3d35-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e3d35-110">EXAMPLES</span></span>

## <span data-ttu-id="e3d35-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e3d35-111">PARAMETERS</span></span>

### <span data-ttu-id="e3d35-112">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e3d35-112">-PassThru</span></span>
<span data-ttu-id="e3d35-113">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="e3d35-113">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e3d35-114">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="e3d35-114">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e3d35-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="e3d35-115">-Profile</span></span>
<span data-ttu-id="e3d35-116">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3d35-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e3d35-117">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="e3d35-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e3d35-118">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="e3d35-118">-ServiceName</span></span>
<span data-ttu-id="e3d35-119">Określa nazwę hostowanej usługi.</span><span class="sxs-lookup"><span data-stu-id="e3d35-119">Specifies the name of the hosted service to start.</span></span>
<span data-ttu-id="e3d35-120">Jeśli nie podano nazwy, polecenie cmdlet rozpoczyna bieżącą usługę hostowaną.</span><span class="sxs-lookup"><span data-stu-id="e3d35-120">If no name is specified, the cmdlet starts the current hosted service.</span></span>

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

### <span data-ttu-id="e3d35-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="e3d35-121">-Slot</span></span>
<span data-ttu-id="e3d35-122">Określa miejsce wdrożenia, w którym ma zostać uruchomiona usługa, czyli przemieszczenie lub produkcja.</span><span class="sxs-lookup"><span data-stu-id="e3d35-122">Specifies the deployment slot in which to start the service, either Staging or Production.</span></span>

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

### <span data-ttu-id="e3d35-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3d35-123">CommonParameters</span></span>
<span data-ttu-id="e3d35-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3d35-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3d35-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3d35-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3d35-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e3d35-126">INPUTS</span></span>

## <span data-ttu-id="e3d35-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e3d35-127">OUTPUTS</span></span>

## <span data-ttu-id="e3d35-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e3d35-128">NOTES</span></span>

## <span data-ttu-id="e3d35-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e3d35-129">RELATED LINKS</span></span>

[<span data-ttu-id="e3d35-130">Remove-AzureService</span><span class="sxs-lookup"><span data-stu-id="e3d35-130">Remove-AzureService</span></span>](./Remove-AzureService.md)

[<span data-ttu-id="e3d35-131">Start — AzureService</span><span class="sxs-lookup"><span data-stu-id="e3d35-131">Start-AzureService</span></span>](./Start-AzureService.md)

[<span data-ttu-id="e3d35-132">Zatrzymaj — AzureService</span><span class="sxs-lookup"><span data-stu-id="e3d35-132">Stop-AzureService</span></span>](./Stop-AzureService.md)


