---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 9FCECA04-9855-461C-9470-85312993C4B1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5bb7bb3e708720b481edc4489d858c70736eac95
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054992"
---
# <span data-ttu-id="308bb-101">Start-AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="308bb-101">Start-AzureVNetGatewayDiagnostics</span></span>

## <span data-ttu-id="308bb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="308bb-102">SYNOPSIS</span></span>
<span data-ttu-id="308bb-103">Rozpoczyna diagnostykę bramy dla bramy VPN.</span><span class="sxs-lookup"><span data-stu-id="308bb-103">Starts gateway diagnostics for a VPN gateway.</span></span>

## <span data-ttu-id="308bb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="308bb-104">SYNTAX</span></span>

```
Start-AzureVNetGatewayDiagnostics -VNetName <String> -CaptureDurationInSeconds <Int32>
 [-ContainerName <String>] -StorageContext <AzureStorageContext> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="308bb-105">Opis</span><span class="sxs-lookup"><span data-stu-id="308bb-105">DESCRIPTION</span></span>
<span data-ttu-id="308bb-106">Polecenie cmdlet **Start-AzureVNetGatewayDiagnostics** rozpoczyna nową sesję diagnostyczną bramy dla bramy wirtualnej sieci prywatnej (VPN).</span><span class="sxs-lookup"><span data-stu-id="308bb-106">The **Start-AzureVNetGatewayDiagnostics** cmdlet starts a new gateway diagnostics session for a virtual private network (VPN) gateway.</span></span>
<span data-ttu-id="308bb-107">W danej chwili może być uruchomiona tylko jedna sesja diagnostyki bramy.</span><span class="sxs-lookup"><span data-stu-id="308bb-107">Only one gateway diagnostics session can run at a time.</span></span>
<span data-ttu-id="308bb-108">Jeśli uruchomisz to polecenie cmdlet, gdy sesja diagnostyki bramy jest uruchomiona, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="308bb-108">If you run this cmdlet while a gateway diagnostics session is running, this cmdlet returns an error.</span></span>

## <span data-ttu-id="308bb-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="308bb-109">EXAMPLES</span></span>

## <span data-ttu-id="308bb-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="308bb-110">PARAMETERS</span></span>

### <span data-ttu-id="308bb-111">-CaptureDurationInSeconds</span><span class="sxs-lookup"><span data-stu-id="308bb-111">-CaptureDurationInSeconds</span></span>
<span data-ttu-id="308bb-112">Określa czas trwania przechwytywania w sekundach.</span><span class="sxs-lookup"><span data-stu-id="308bb-112">Specifies the capture duration in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="308bb-113">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="308bb-113">-ContainerName</span></span>
<span data-ttu-id="308bb-114">Określa nazwę kontenera platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="308bb-114">Specifies the name of an Azure container.</span></span>
<span data-ttu-id="308bb-115">To polecenie cmdlet przechowuje wyniki w kontenerze, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="308bb-115">This cmdlet stores results in the container that this parameter specifies.</span></span>

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

### <span data-ttu-id="308bb-116">-Profile</span><span class="sxs-lookup"><span data-stu-id="308bb-116">-Profile</span></span>
<span data-ttu-id="308bb-117">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="308bb-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="308bb-118">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="308bb-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="308bb-119">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="308bb-119">-StorageContext</span></span>
<span data-ttu-id="308bb-120">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="308bb-120">Specifies an Azure storage context.</span></span>
<span data-ttu-id="308bb-121">To polecenie cmdlet przechowuje wyniki, korzystając z kontekstu magazynu określanego przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="308bb-121">This cmdlet stores results by using the storage context that this parameter specifies.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="308bb-122">-VNetName</span><span class="sxs-lookup"><span data-stu-id="308bb-122">-VNetName</span></span>
<span data-ttu-id="308bb-123">Określa sieć wirtualną zawierającą wirtualną bramę sieciową, dla którego to polecenie cmdlet wykonuje testy diagnostyczne.</span><span class="sxs-lookup"><span data-stu-id="308bb-123">Specifies the virtual network that contains a virtual network gateway for which this cmdlet runs diagnostics.</span></span>

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

### <span data-ttu-id="308bb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="308bb-124">CommonParameters</span></span>
<span data-ttu-id="308bb-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="308bb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="308bb-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="308bb-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="308bb-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="308bb-127">INPUTS</span></span>

## <span data-ttu-id="308bb-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="308bb-128">OUTPUTS</span></span>

## <span data-ttu-id="308bb-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="308bb-129">NOTES</span></span>

## <span data-ttu-id="308bb-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="308bb-130">RELATED LINKS</span></span>

[<span data-ttu-id="308bb-131">Get-AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="308bb-131">Get-AzureVNetGatewayDiagnostics</span></span>](./Get-AzureVNetGatewayDiagnostics.md)

[<span data-ttu-id="308bb-132">Zatrzymaj — AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="308bb-132">Stop-AzureVNetGatewayDiagnostics</span></span>](./Stop-AzureVNetGatewayDiagnostics.md)


