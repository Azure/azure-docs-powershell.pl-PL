---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 128AD64D-709A-4B59-B233-4221A9120AE1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4803fd24952066c4dcea72daaf0c999b64ae4c5d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055463"
---
# <span data-ttu-id="824c5-101">Remove-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="824c5-101">Remove-AzureApplicationGateway</span></span>

## <span data-ttu-id="824c5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="824c5-102">SYNOPSIS</span></span>
<span data-ttu-id="824c5-103">Usuwa bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="824c5-103">Removes an application gateway.</span></span>

## <span data-ttu-id="824c5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="824c5-104">SYNTAX</span></span>

```
Remove-AzureApplicationGateway -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="824c5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="824c5-105">DESCRIPTION</span></span>
<span data-ttu-id="824c5-106">Polecenie cmdlet **Remove-AzureApplicationGateway** usuwa bramę Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="824c5-106">The **Remove-AzureApplicationGateway** cmdlet removes an application gateway.</span></span>

## <span data-ttu-id="824c5-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="824c5-107">EXAMPLES</span></span>

### <span data-ttu-id="824c5-108">Przykład 1: usuwanie bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="824c5-108">Example 1: Remove an application gateway</span></span>
```
PS C:\> Remove-AzureApplicationGateway -Name "ApplicationGateway06"
```

<span data-ttu-id="824c5-109">To polecenie usuwa bramkę Application Gateway o nazwie ApplicationGateway06.</span><span class="sxs-lookup"><span data-stu-id="824c5-109">This command removes the application gateway named ApplicationGateway06.</span></span>

## <span data-ttu-id="824c5-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="824c5-110">PARAMETERS</span></span>

### <span data-ttu-id="824c5-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="824c5-111">-Name</span></span>
<span data-ttu-id="824c5-112">Określa nazwę bramy aplikacji, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="824c5-112">Specifies the name of the application gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="824c5-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="824c5-113">-Profile</span></span>
<span data-ttu-id="824c5-114">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="824c5-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="824c5-115">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="824c5-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="824c5-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="824c5-116">CommonParameters</span></span>
<span data-ttu-id="824c5-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="824c5-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="824c5-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="824c5-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="824c5-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="824c5-119">INPUTS</span></span>

### <span data-ttu-id="824c5-120">System. String</span><span class="sxs-lookup"><span data-stu-id="824c5-120">System.String</span></span>

## <span data-ttu-id="824c5-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="824c5-121">OUTPUTS</span></span>

### <span data-ttu-id="824c5-122">Microsoft. platformy windowsazure. Management. ApplicationGateway. MODELES. ApplicationGatewayOperationResponse</span><span class="sxs-lookup"><span data-stu-id="824c5-122">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="824c5-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="824c5-123">NOTES</span></span>

## <span data-ttu-id="824c5-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="824c5-124">RELATED LINKS</span></span>

[<span data-ttu-id="824c5-125">Get-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="824c5-125">Get-AzureApplicationGateway</span></span>](./Get-AzureApplicationGateway.md)

[<span data-ttu-id="824c5-126">Nowe — AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="824c5-126">New-AzureApplicationGateway</span></span>](./New-AzureApplicationGateway.md)

[<span data-ttu-id="824c5-127">Start — AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="824c5-127">Start-AzureApplicationGateway</span></span>](./Start-AzureApplicationGateway.md)

[<span data-ttu-id="824c5-128">Zatrzymaj — AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="824c5-128">Stop-AzureApplicationGateway</span></span>](./Stop-AzureApplicationGateway.md)

[<span data-ttu-id="824c5-129">Update-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="824c5-129">Update-AzureApplicationGateway</span></span>](./Update-AzureApplicationGateway.md)


