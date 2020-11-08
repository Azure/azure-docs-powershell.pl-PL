---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 0AED21E8-A638-4019-9B23-447472E56C7A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 202066cfc2649b0f56810123e211bbeb5d69720f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054636"
---
# <span data-ttu-id="2545c-101">Get-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2545c-101">Get-AzureApplicationGateway</span></span>

## <span data-ttu-id="2545c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2545c-102">SYNOPSIS</span></span>
<span data-ttu-id="2545c-103">Pobiera bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="2545c-103">Gets an Application Gateway.</span></span>

## <span data-ttu-id="2545c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2545c-104">SYNTAX</span></span>

```
Get-AzureApplicationGateway [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2545c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2545c-105">DESCRIPTION</span></span>
<span data-ttu-id="2545c-106">Polecenie cmdlet **Get-AzureApplicationGateway** pobiera istniejącą bramę aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2545c-106">The **Get-AzureApplicationGateway** cmdlet gets an existing Azure Application Gateway.</span></span>

## <span data-ttu-id="2545c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2545c-107">EXAMPLES</span></span>

### <span data-ttu-id="2545c-108">Przykład 1: uzyskiwanie bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="2545c-108">Example 1: Get an Application Gateway</span></span>
```
PS C:\> Get-AzureApplicationGateway -Name "ApplicationGateway06"
```

<span data-ttu-id="2545c-109">To polecenie pobiera bramkę Application Gateway o nazwie ApplicationGateway06.</span><span class="sxs-lookup"><span data-stu-id="2545c-109">This command gets the Application Gateway named ApplicationGateway06.</span></span>

### <span data-ttu-id="2545c-110">Przykład 2: pobieranie wszystkich bram aplikacji</span><span class="sxs-lookup"><span data-stu-id="2545c-110">Example 2: Get all Application Gateways</span></span>
```
PS C:\> Get-AzureApplicationGateway
```

<span data-ttu-id="2545c-111">To polecenie pobiera wszystkie bramy aplikacji w ramach abonamentu.</span><span class="sxs-lookup"><span data-stu-id="2545c-111">This command gets all the Application Gateways under your subscription.</span></span>

## <span data-ttu-id="2545c-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2545c-112">PARAMETERS</span></span>

### <span data-ttu-id="2545c-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2545c-113">-Name</span></span>
<span data-ttu-id="2545c-114">Określa nazwę bramy aplikacji, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2545c-114">Specifies the name of the Application Gateway that this cmdlet gets.</span></span>

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

### <span data-ttu-id="2545c-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="2545c-115">-Profile</span></span>
<span data-ttu-id="2545c-116">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2545c-116">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="2545c-117">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="2545c-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2545c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2545c-118">CommonParameters</span></span>
<span data-ttu-id="2545c-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2545c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2545c-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2545c-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2545c-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2545c-121">INPUTS</span></span>

### <span data-ttu-id="2545c-122">System. String</span><span class="sxs-lookup"><span data-stu-id="2545c-122">System.String</span></span>

## <span data-ttu-id="2545c-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2545c-123">OUTPUTS</span></span>

### <span data-ttu-id="2545c-124">Microsoft. Azure. Networking. ApplicationGatewayObjectModel. ApplicationGateway, IEnumerable<Microsoft. Azure. Networking. ApplicationGatewayObjectModel. ApplicationGateway></span><span class="sxs-lookup"><span data-stu-id="2545c-124">Microsoft.Azure.Networking.ApplicationGatewayObjectModel.ApplicationGateway, IEnumerable<Microsoft.Azure.Networking.ApplicationGatewayObjectModel.ApplicationGateway></span></span>

## <span data-ttu-id="2545c-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2545c-125">NOTES</span></span>

## <span data-ttu-id="2545c-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2545c-126">RELATED LINKS</span></span>

[<span data-ttu-id="2545c-127">Nowe — AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2545c-127">New-AzureApplicationGateway</span></span>](./New-AzureApplicationGateway.md)

[<span data-ttu-id="2545c-128">Remove-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2545c-128">Remove-AzureApplicationGateway</span></span>](./Remove-AzureApplicationGateway.md)

[<span data-ttu-id="2545c-129">Start — AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2545c-129">Start-AzureApplicationGateway</span></span>](./Start-AzureApplicationGateway.md)

[<span data-ttu-id="2545c-130">Zatrzymaj — AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2545c-130">Stop-AzureApplicationGateway</span></span>](./Stop-AzureApplicationGateway.md)

[<span data-ttu-id="2545c-131">Update-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2545c-131">Update-AzureApplicationGateway</span></span>](./Update-AzureApplicationGateway.md)


