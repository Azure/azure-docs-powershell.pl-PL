---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: DA5689DF-AA4A-4161-89B0-8055BF384274
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7b71367ac18a753fad5425d0073b55cacb413e4b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054738"
---
# <span data-ttu-id="37ec1-101">Start-AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="37ec1-101">Start-AzureVirtualNetworkGatewayDiagnostics</span></span>

## <span data-ttu-id="37ec1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="37ec1-102">SYNOPSIS</span></span>
<span data-ttu-id="37ec1-103">Rozpoczyna diagnostykę bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="37ec1-103">Starts diagnostics for a virtual network gateway.</span></span>

## <span data-ttu-id="37ec1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="37ec1-104">SYNTAX</span></span>

```
Start-AzureVirtualNetworkGatewayDiagnostics -GatewayId <String> [-CaptureDurationInSeconds <Int32>]
 [-ContainerName <String>] [-StorageContext <AzureStorageContext>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="37ec1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="37ec1-105">DESCRIPTION</span></span>
<span data-ttu-id="37ec1-106">Polecenie cmdlet **Start-AzureVirtualNetworkGatewayDiagnostics** rozpoczyna nową sesję diagnostyczną bramy dla bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="37ec1-106">The **Start-AzureVirtualNetworkGatewayDiagnostics** cmdlet starts a new gateway diagnostics session for a virtual network gateway.</span></span>
<span data-ttu-id="37ec1-107">W danej chwili może być uruchomiona tylko jedna sesja diagnostyki bramy.</span><span class="sxs-lookup"><span data-stu-id="37ec1-107">Only one gateway diagnostics session can run at a time.</span></span>
<span data-ttu-id="37ec1-108">Jeśli uruchomisz to polecenie cmdlet, gdy sesja diagnostyki bramy jest uruchomiona, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="37ec1-108">If you run this cmdlet while a gateway diagnostics session is running, this cmdlet returns an error.</span></span>

## <span data-ttu-id="37ec1-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="37ec1-109">EXAMPLES</span></span>

## <span data-ttu-id="37ec1-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="37ec1-110">PARAMETERS</span></span>

### <span data-ttu-id="37ec1-111">-CaptureDurationInSeconds</span><span class="sxs-lookup"><span data-stu-id="37ec1-111">-CaptureDurationInSeconds</span></span>
<span data-ttu-id="37ec1-112">Określa czas trwania przechwytywania w sekundach.</span><span class="sxs-lookup"><span data-stu-id="37ec1-112">Specifies the capture duration in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37ec1-113">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="37ec1-113">-ContainerName</span></span>
<span data-ttu-id="37ec1-114">Określa nazwę kontenera platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="37ec1-114">Specifies the name of an Azure container.</span></span>
<span data-ttu-id="37ec1-115">To polecenie cmdlet przechowuje wyniki w kontenerze, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="37ec1-115">This cmdlet stores results in the container that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37ec1-116">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="37ec1-116">-GatewayId</span></span>
<span data-ttu-id="37ec1-117">Określa identyfikator bramy.</span><span class="sxs-lookup"><span data-stu-id="37ec1-117">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="37ec1-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="37ec1-118">-Profile</span></span>
<span data-ttu-id="37ec1-119">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37ec1-119">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="37ec1-120">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="37ec1-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="37ec1-121">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="37ec1-121">-StorageContext</span></span>
<span data-ttu-id="37ec1-122">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="37ec1-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="37ec1-123">To polecenie cmdlet przechowuje wyniki, korzystając z kontekstu magazynu określanego przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="37ec1-123">This cmdlet stores results by using the storage context that this parameter specifies.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37ec1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37ec1-124">CommonParameters</span></span>
<span data-ttu-id="37ec1-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37ec1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37ec1-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37ec1-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37ec1-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="37ec1-127">INPUTS</span></span>

## <span data-ttu-id="37ec1-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="37ec1-128">OUTPUTS</span></span>

## <span data-ttu-id="37ec1-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="37ec1-129">NOTES</span></span>

## <span data-ttu-id="37ec1-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="37ec1-130">RELATED LINKS</span></span>

[<span data-ttu-id="37ec1-131">Get-AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="37ec1-131">Get-AzureVirtualNetworkGatewayDiagnostics</span></span>](./Get-AzureVirtualNetworkGatewayDiagnostics.md)

[<span data-ttu-id="37ec1-132">Zatrzymaj — AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="37ec1-132">Stop-AzureVirtualNetworkGatewayDiagnostics</span></span>](./Stop-AzureVirtualNetworkGatewayDiagnostics.md)


