---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 58DABEB0-D3B6-478B-9B83-80E4C67A7792
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1d4717e795bcfea9728cbabb1b7c788713907aaa
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055536"
---
# <span data-ttu-id="5c5ad-101">Get-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="5c5ad-101">Get-AzureRemoteAppVNet</span></span>

## <span data-ttu-id="5c5ad-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5c5ad-102">SYNOPSIS</span></span>
<span data-ttu-id="5c5ad-103">Pobiera informacje o wirtualnych sieciach Azure RemoteApp na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="5c5ad-103">Retrieves information about Azure RemoteApp virtual networks in Azure.</span></span>

## <span data-ttu-id="5c5ad-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5c5ad-104">SYNTAX</span></span>

```
Get-AzureRemoteAppVNet [[-VNetName] <String>] [-IncludeSharedKey] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="5c5ad-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5c5ad-105">DESCRIPTION</span></span>
<span data-ttu-id="5c5ad-106">Polecenie cmdlet **Get-AzureRemoteAppVNet** pobiera informacje o wirtualnych sieciach funkcji Azure RemoteApp na platformie Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="5c5ad-106">The **Get-AzureRemoteAppVNet** cmdlet retrieves information about Azure RemoteApp virtual networks in Microsoft Azure.</span></span>
<span data-ttu-id="5c5ad-107">To polecenie cmdlet zwraca obiekt zawierający informacje o określonej sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5c5ad-107">This cmdlet returns an object that contains information about a specified virtual network.</span></span>
<span data-ttu-id="5c5ad-108">Jeśli nie określono sieci wirtualnej, to polecenie cmdlet zwraca informacje o wszystkich sieciach wirtualnych w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="5c5ad-108">If no virtual network is specified, this cmdlet returns information about all the virtual networks in the current subscription.</span></span>

## <span data-ttu-id="5c5ad-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5c5ad-109">EXAMPLES</span></span>

### <span data-ttu-id="5c5ad-110">Przykład 1: pobieranie informacji o sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="5c5ad-110">Example 1: Retrieve information about a virtual network</span></span>
```
PS C:\> Get-AzureRemoteAppVNet -VNetName "ContosoVNet"
```

<span data-ttu-id="5c5ad-111">To polecenie pobiera informacje o sieci wirtualnej o nazwie ContosoVNet.</span><span class="sxs-lookup"><span data-stu-id="5c5ad-111">This command gets information about the virtual network named ContosoVNet.</span></span>

## <span data-ttu-id="5c5ad-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5c5ad-112">PARAMETERS</span></span>

### <span data-ttu-id="5c5ad-113">-IncludeSharedKey</span><span class="sxs-lookup"><span data-stu-id="5c5ad-113">-IncludeSharedKey</span></span>
<span data-ttu-id="5c5ad-114">Wskazuje, że w tym poleceniu cmdlet jest uwzględniana wartość klucza współdzielonego w informacjach pobieranych na temat sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5c5ad-114">Indicates that this cmdlet includes the shared key value in the information it retrieves about the virtual network.</span></span>

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

### <span data-ttu-id="5c5ad-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="5c5ad-115">-Profile</span></span>
<span data-ttu-id="5c5ad-116">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c5ad-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5c5ad-117">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="5c5ad-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5c5ad-118">-VNetName</span><span class="sxs-lookup"><span data-stu-id="5c5ad-118">-VNetName</span></span>
<span data-ttu-id="5c5ad-119">Określa nazwę sieci wirtualnej usługi Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="5c5ad-119">Specifies the name of the Azure RemoteApp virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: True
```

### <span data-ttu-id="5c5ad-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c5ad-120">CommonParameters</span></span>
<span data-ttu-id="5c5ad-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c5ad-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c5ad-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c5ad-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c5ad-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5c5ad-123">INPUTS</span></span>

## <span data-ttu-id="5c5ad-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5c5ad-124">OUTPUTS</span></span>

## <span data-ttu-id="5c5ad-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5c5ad-125">NOTES</span></span>

## <span data-ttu-id="5c5ad-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5c5ad-126">RELATED LINKS</span></span>

[<span data-ttu-id="5c5ad-127">Set-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="5c5ad-127">Set-AzureRemoteAppVNet</span></span>](./Set-AzureRemoteAppVNet.md)


