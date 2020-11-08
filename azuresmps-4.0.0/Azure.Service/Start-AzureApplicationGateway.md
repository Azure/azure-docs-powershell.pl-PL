---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: D50984B7-FD97-4713-8E56-1C06D2B008E3
online version: ''
schema: 2.0.0
ms.openlocfilehash: a01d59d6a0755b3763eaef9b7532326ca0ffd402
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054745"
---
# <span data-ttu-id="9bc91-101">Start-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9bc91-101">Start-AzureApplicationGateway</span></span>

## <span data-ttu-id="9bc91-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9bc91-102">SYNOPSIS</span></span>
<span data-ttu-id="9bc91-103">Uruchamia bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="9bc91-103">Starts an application gateway.</span></span>

## <span data-ttu-id="9bc91-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9bc91-104">SYNTAX</span></span>

```
Start-AzureApplicationGateway -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9bc91-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9bc91-105">DESCRIPTION</span></span>
<span data-ttu-id="9bc91-106">Polecenie cmdlet **Start-AzureApplicationGateway** uruchamia bramę Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="9bc91-106">The **Start-AzureApplicationGateway** cmdlet starts an application gateway.</span></span>

## <span data-ttu-id="9bc91-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9bc91-107">EXAMPLES</span></span>

### <span data-ttu-id="9bc91-108">Przykład 1. Uruchom bramę aplikacji</span><span class="sxs-lookup"><span data-stu-id="9bc91-108">Example 1: Start an application gateway</span></span>
```
PS C:\> Start-AzureApplicationGateway -Name "ApplicationGateway06"
```

<span data-ttu-id="9bc91-109">To polecenie uruchamia bramkę Application Gateway o nazwie ApplicationGateway06.</span><span class="sxs-lookup"><span data-stu-id="9bc91-109">This command starts the application gateway named ApplicationGateway06.</span></span>

## <span data-ttu-id="9bc91-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9bc91-110">PARAMETERS</span></span>

### <span data-ttu-id="9bc91-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9bc91-111">-Name</span></span>
<span data-ttu-id="9bc91-112">Określa nazwę bramy aplikacji, która jest uruchamiana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9bc91-112">Specifies the name of the application gateway that this cmdlet starts.</span></span>

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

### <span data-ttu-id="9bc91-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="9bc91-113">-Profile</span></span>
<span data-ttu-id="9bc91-114">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9bc91-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="9bc91-115">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="9bc91-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9bc91-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bc91-116">CommonParameters</span></span>
<span data-ttu-id="9bc91-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bc91-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bc91-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bc91-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bc91-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9bc91-119">INPUTS</span></span>

### <span data-ttu-id="9bc91-120">System. String</span><span class="sxs-lookup"><span data-stu-id="9bc91-120">System.String</span></span>

## <span data-ttu-id="9bc91-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9bc91-121">OUTPUTS</span></span>

### <span data-ttu-id="9bc91-122">Microsoft. platformy windowsazure. Management. ApplicationGateway. MODELES. ApplicationGatewayOperationResponse</span><span class="sxs-lookup"><span data-stu-id="9bc91-122">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="9bc91-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9bc91-123">NOTES</span></span>

## <span data-ttu-id="9bc91-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9bc91-124">RELATED LINKS</span></span>

[<span data-ttu-id="9bc91-125">Get-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9bc91-125">Get-AzureApplicationGateway</span></span>](./Get-AzureApplicationGateway.md)

[<span data-ttu-id="9bc91-126">Nowe — AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9bc91-126">New-AzureApplicationGateway</span></span>](./New-AzureApplicationGateway.md)

[<span data-ttu-id="9bc91-127">Remove-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9bc91-127">Remove-AzureApplicationGateway</span></span>](./Remove-AzureApplicationGateway.md)

[<span data-ttu-id="9bc91-128">Zatrzymaj — AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9bc91-128">Stop-AzureApplicationGateway</span></span>](./Stop-AzureApplicationGateway.md)

[<span data-ttu-id="9bc91-129">Update-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9bc91-129">Update-AzureApplicationGateway</span></span>](./Update-AzureApplicationGateway.md)


