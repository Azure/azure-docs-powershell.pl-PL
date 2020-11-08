---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 17BA2ED5-E347-45C0-AF20-CDD288469514
online version: ''
schema: 2.0.0
ms.openlocfilehash: a07afcadb2207f2e4377601abfa6094bc3293328
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055374"
---
# <span data-ttu-id="3a985-101">Stop-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3a985-101">Stop-AzureApplicationGateway</span></span>

## <span data-ttu-id="3a985-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3a985-102">SYNOPSIS</span></span>
<span data-ttu-id="3a985-103">Zatrzymuje bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="3a985-103">Stops an application gateway.</span></span>

## <span data-ttu-id="3a985-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3a985-104">SYNTAX</span></span>

```
Stop-AzureApplicationGateway -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3a985-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3a985-105">DESCRIPTION</span></span>
<span data-ttu-id="3a985-106">Polecenie cmdlet **stop-AzureApplicationGateway** zatrzymuje bramę Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="3a985-106">The **Stop-AzureApplicationGateway** cmdlet stops an application gateway.</span></span>

## <span data-ttu-id="3a985-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3a985-107">EXAMPLES</span></span>

### <span data-ttu-id="3a985-108">Przykład 1: zatrzymywanie bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="3a985-108">Example 1: Stop an application gateway</span></span>
```
PS C:\> Stop-AzureApplicationGateway -Name "ApplicationGateway06"
```

<span data-ttu-id="3a985-109">To polecenie zatrzymuje bramkę Application Gateway o nazwie ApplicationGateway06.</span><span class="sxs-lookup"><span data-stu-id="3a985-109">This command stops the application gateway named ApplicationGateway06.</span></span>

## <span data-ttu-id="3a985-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3a985-110">PARAMETERS</span></span>

### <span data-ttu-id="3a985-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3a985-111">-Name</span></span>
<span data-ttu-id="3a985-112">Określa nazwę bramy aplikacji, która zostanie zatrzymana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a985-112">Specifies the name of the application gateway that this cmdlet stops.</span></span>

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

### <span data-ttu-id="3a985-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="3a985-113">-Profile</span></span>
<span data-ttu-id="3a985-114">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a985-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3a985-115">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="3a985-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3a985-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a985-116">CommonParameters</span></span>
<span data-ttu-id="3a985-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a985-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a985-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a985-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a985-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3a985-119">INPUTS</span></span>

### <span data-ttu-id="3a985-120">System. String</span><span class="sxs-lookup"><span data-stu-id="3a985-120">System.String</span></span>

## <span data-ttu-id="3a985-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3a985-121">OUTPUTS</span></span>

### <span data-ttu-id="3a985-122">Microsoft. platformy windowsazure. Management. ApplicationGateway. MODELES. ApplicationGatewayOperationResponse</span><span class="sxs-lookup"><span data-stu-id="3a985-122">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="3a985-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3a985-123">NOTES</span></span>

## <span data-ttu-id="3a985-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3a985-124">RELATED LINKS</span></span>

[<span data-ttu-id="3a985-125">Get-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3a985-125">Get-AzureApplicationGateway</span></span>](./Get-AzureApplicationGateway.md)

[<span data-ttu-id="3a985-126">Nowe — AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3a985-126">New-AzureApplicationGateway</span></span>](./New-AzureApplicationGateway.md)

[<span data-ttu-id="3a985-127">Remove-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3a985-127">Remove-AzureApplicationGateway</span></span>](./Remove-AzureApplicationGateway.md)

[<span data-ttu-id="3a985-128">Start — AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3a985-128">Start-AzureApplicationGateway</span></span>](./Start-AzureApplicationGateway.md)

[<span data-ttu-id="3a985-129">Update-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3a985-129">Update-AzureApplicationGateway</span></span>](./Update-AzureApplicationGateway.md)
