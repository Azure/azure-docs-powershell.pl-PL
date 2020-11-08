---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 4024D20D-46DF-4ED8-A091-E6E17F840E40
online version: ''
schema: 2.0.0
ms.openlocfilehash: 92c6ba8827906fbfc51b121e4500dea3ec4555d9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055245"
---
# <span data-ttu-id="2434c-101">Get-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="2434c-101">Get-AzureVNetGateway</span></span>

## <span data-ttu-id="2434c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2434c-102">SYNOPSIS</span></span>
<span data-ttu-id="2434c-103">Pobiera stan bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2434c-103">Gets the status of a virtual network gateway.</span></span>

## <span data-ttu-id="2434c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2434c-104">SYNTAX</span></span>

```
Get-AzureVNetGateway -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2434c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2434c-105">DESCRIPTION</span></span>
<span data-ttu-id="2434c-106">Polecenie cmdlet **Get-AzureVNetGateway** Pobiera stan istniejącej bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2434c-106">The **Get-AzureVNetGateway** cmdlet gets the status of an existing virtual network gateway.</span></span>

## <span data-ttu-id="2434c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2434c-107">EXAMPLES</span></span>

### <span data-ttu-id="2434c-108">Przykład 1: uzyskiwanie statusu bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="2434c-108">Example 1: Get the status of a virtual network gateway</span></span>
```
PS C:\> Get-AzureVNetGateway -VNetName "ContosoVN07"
```

<span data-ttu-id="2434c-109">To polecenie uzyskuje stan bramy sieci wirtualnej dla sieci wirtualnej o nazwie ContosoVN07.</span><span class="sxs-lookup"><span data-stu-id="2434c-109">This command gets that status of the virtual network gateway for the virtual network named ContosoVN07.</span></span>

## <span data-ttu-id="2434c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2434c-110">PARAMETERS</span></span>

### <span data-ttu-id="2434c-111">-Profile</span><span class="sxs-lookup"><span data-stu-id="2434c-111">-Profile</span></span>
<span data-ttu-id="2434c-112">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2434c-112">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="2434c-113">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="2434c-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2434c-114">-VNetName</span><span class="sxs-lookup"><span data-stu-id="2434c-114">-VNetName</span></span>
<span data-ttu-id="2434c-115">Określa sieć wirtualną zawierającą wirtualną bramę sieciową, dla której to polecenie cmdlet pobiera stan.</span><span class="sxs-lookup"><span data-stu-id="2434c-115">Specifies the virtual network that contains the virtual network gateway for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="2434c-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2434c-116">CommonParameters</span></span>
<span data-ttu-id="2434c-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2434c-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2434c-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2434c-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2434c-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2434c-119">INPUTS</span></span>

## <span data-ttu-id="2434c-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2434c-120">OUTPUTS</span></span>

## <span data-ttu-id="2434c-121">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2434c-121">NOTES</span></span>

## <span data-ttu-id="2434c-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2434c-122">RELATED LINKS</span></span>

[<span data-ttu-id="2434c-123">Nowe — AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="2434c-123">New-AzureVNetGateway</span></span>](./New-AzureVNetGateway.md)

[<span data-ttu-id="2434c-124">Remove-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="2434c-124">Remove-AzureVNetGateway</span></span>](./Remove-AzureVNetGateway.md)

[<span data-ttu-id="2434c-125">Resetowanie — AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="2434c-125">Reset-AzureVNetGateway</span></span>](./Reset-AzureVNetGateway.md)

[<span data-ttu-id="2434c-126">Zmienianie rozmiaru — AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="2434c-126">Resize-AzureVNetGateway</span></span>](./Resize-AzureVNetGateway.md)

[<span data-ttu-id="2434c-127">Set-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="2434c-127">Set-AzureVNetGatewayKey</span></span>](./Set-AzureVNetGatewayKey.md)


