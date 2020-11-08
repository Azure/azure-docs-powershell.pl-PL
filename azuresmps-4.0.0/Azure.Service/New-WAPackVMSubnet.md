---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 83D18A17-94A4-4FB8-9DA6-F652D5BB84C7
online version: ''
schema: 2.0.0
ms.openlocfilehash: bf06561ac5f8c9e0c19edb88b7a8ff5ef816c609
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054852"
---
# <span data-ttu-id="353a5-101">New-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="353a5-101">New-WAPackVMSubnet</span></span>

## <span data-ttu-id="353a5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="353a5-102">SYNOPSIS</span></span>
<span data-ttu-id="353a5-103">Tworzy podsieć maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="353a5-103">Creates a virtual machine subnet.</span></span>

## <span data-ttu-id="353a5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="353a5-104">SYNTAX</span></span>

```
New-WAPackVMSubnet -VNet <VMNetwork> -Name <String> -Subnet <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="353a5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="353a5-105">DESCRIPTION</span></span>
<span data-ttu-id="353a5-106">Polecenie cmdlet **New-WAPackVMSubnet** tworzy podsieć maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="353a5-106">The **New-WAPackVMSubnet** cmdlet creates a virtual machine subnet.</span></span>

## <span data-ttu-id="353a5-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="353a5-107">EXAMPLES</span></span>

### <span data-ttu-id="353a5-108">Przykład 1. Tworzenie podsieci maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="353a5-108">Example 1: Create a virtual machine subnet</span></span>
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet01"
PS C:\> New-WAPackVMSubnet -VNet $VNet -Name "ContosoVMSubnet01" -Subnet "192.168.1.0/24"
```

<span data-ttu-id="353a5-109">Pierwsze polecenie najpierw pobiera sieć maszyny wirtualnej, do której chcemy dodać nową podsieć maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="353a5-109">The first command first retrieves the virtual machine network to which we want to add a new virtual machine subnet.</span></span>
<span data-ttu-id="353a5-110">Ta sieć maszyny wirtualnej nosi nazwę ContosoVNet01.</span><span class="sxs-lookup"><span data-stu-id="353a5-110">This virtual machine network is named ContosoVNet01.</span></span>

<span data-ttu-id="353a5-111">Drugie polecenie tworzy podsieć maszyny wirtualnej przy użyciu poprzedniej pobranej sieci maszyny wirtualnej, nazwy ContosoVMSubnet01 oraz podsieci 192.168.1.0/24.</span><span class="sxs-lookup"><span data-stu-id="353a5-111">The second command creates a virtual machine subnet using the previously retrieve virtual machine network, a name ContosoVMSubnet01 and a subnet 192.168.1.0/24.</span></span>

## <span data-ttu-id="353a5-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="353a5-112">PARAMETERS</span></span>

### <span data-ttu-id="353a5-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="353a5-113">-Name</span></span>
<span data-ttu-id="353a5-114">Określa nazwę podsieci maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="353a5-114">Specifies a name for the virtual machine subnet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="353a5-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="353a5-115">-Profile</span></span>
<span data-ttu-id="353a5-116">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="353a5-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="353a5-117">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="353a5-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="353a5-118">-Podsieć</span><span class="sxs-lookup"><span data-stu-id="353a5-118">-Subnet</span></span>
<span data-ttu-id="353a5-119">Określa podsieć dla podsieci maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="353a5-119">Specifies a subnet for the virtual machine subnet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="353a5-120">-VNet</span><span class="sxs-lookup"><span data-stu-id="353a5-120">-VNet</span></span>
<span data-ttu-id="353a5-121">Określa sieć wirtualnej skojarzoną z podsiecią maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="353a5-121">Specifies a VNet associated with the virtual machine subnet.</span></span>

```yaml
Type: VMNetwork
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="353a5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="353a5-122">CommonParameters</span></span>
<span data-ttu-id="353a5-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="353a5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="353a5-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="353a5-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="353a5-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="353a5-125">INPUTS</span></span>

## <span data-ttu-id="353a5-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="353a5-126">OUTPUTS</span></span>

## <span data-ttu-id="353a5-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="353a5-127">NOTES</span></span>

## <span data-ttu-id="353a5-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="353a5-128">RELATED LINKS</span></span>

[<span data-ttu-id="353a5-129">Get-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="353a5-129">Get-WAPackVMSubnet</span></span>](./Get-WAPackVMSubnet.md)

[<span data-ttu-id="353a5-130">Get-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="353a5-130">Get-WAPackVNet</span></span>](./Get-WAPackVNet.md)

[<span data-ttu-id="353a5-131">Remove-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="353a5-131">Remove-WAPackVMSubnet</span></span>](./Remove-WAPackVMSubnet.md)


