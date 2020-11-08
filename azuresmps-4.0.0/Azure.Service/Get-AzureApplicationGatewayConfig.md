---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: A2F0ECAD-595C-45E6-98AC-2C7DB8E4BEF0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4dac85bf4c8b3d0a0f0f4b27cd249a98e020be7d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054631"
---
# <span data-ttu-id="bd72b-101">Get-AzureApplicationGatewayConfig</span><span class="sxs-lookup"><span data-stu-id="bd72b-101">Get-AzureApplicationGatewayConfig</span></span>

## <span data-ttu-id="bd72b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bd72b-102">SYNOPSIS</span></span>
<span data-ttu-id="bd72b-103">Pobiera kontekst konfiguracji bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="bd72b-103">Gets an Application Gateway configuration context.</span></span>

## <span data-ttu-id="bd72b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bd72b-104">SYNTAX</span></span>

```
Get-AzureApplicationGatewayConfig -Name <String> [-ExportToFile <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="bd72b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bd72b-105">DESCRIPTION</span></span>
<span data-ttu-id="bd72b-106">Polecenie cmdlet **Get-AzureApplicationGatewayConfig umożliwia pobranie** kontekstu konfiguracji bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="bd72b-106">The **Get-AzureApplicationGatewayConfig** cmdlet gets an Azure Application Gateway configuration context.</span></span>
<span data-ttu-id="bd72b-107">Kontekst obejmuje zarówno obiekt konfiguracji, jak i konfigurację XML.</span><span class="sxs-lookup"><span data-stu-id="bd72b-107">A context includes both a configuration object and XML configuration.</span></span>
<span data-ttu-id="bd72b-108">Możesz zapisać konfigurację XML w pliku.</span><span class="sxs-lookup"><span data-stu-id="bd72b-108">You can save the XML configuration to a file.</span></span>

## <span data-ttu-id="bd72b-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bd72b-109">EXAMPLES</span></span>

### <span data-ttu-id="bd72b-110">Przykład 1: pobranie konfiguracji bramy aplikacji i zapisanie jej w pliku</span><span class="sxs-lookup"><span data-stu-id="bd72b-110">Example 1: Get an Application Gateway configuration and save it to a file</span></span>
```
PS C:\> Get-AzureApplicationGatewayConfig -Name "ApplicationGateway06" -ExportToFile "D:\config.xml"
```

<span data-ttu-id="bd72b-111">To polecenie pobiera konfigurację bramy Application Gateway o nazwie ApplicationGateway06.</span><span class="sxs-lookup"><span data-stu-id="bd72b-111">This command gets the configuration for an Application Gateway named ApplicationGateway06.</span></span>
<span data-ttu-id="bd72b-112">Polecenie zapisuje je w pliku w określonej ścieżce.</span><span class="sxs-lookup"><span data-stu-id="bd72b-112">The command saves it in the file in the specified path.</span></span>

## <span data-ttu-id="bd72b-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bd72b-113">PARAMETERS</span></span>

### <span data-ttu-id="bd72b-114">-ExportToFile</span><span class="sxs-lookup"><span data-stu-id="bd72b-114">-ExportToFile</span></span>
<span data-ttu-id="bd72b-115">Określa ścieżkę pliku, do którego to polecenie cmdlet zapisuje konfigurację w formacie XML.</span><span class="sxs-lookup"><span data-stu-id="bd72b-115">Specifies a file path to which this cmdlet saves the configuration in XML format.</span></span>

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

### <span data-ttu-id="bd72b-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bd72b-116">-Name</span></span>
<span data-ttu-id="bd72b-117">Określa nazwę bramy aplikacji, dla której to polecenie cmdlet pobiera informacje o konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="bd72b-117">Specifies the name of the Application Gateway for which this cmdlet gets configuration information.</span></span>

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

### <span data-ttu-id="bd72b-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="bd72b-118">-Profile</span></span>
<span data-ttu-id="bd72b-119">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd72b-119">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="bd72b-120">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="bd72b-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="bd72b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd72b-121">CommonParameters</span></span>
<span data-ttu-id="bd72b-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd72b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd72b-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd72b-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd72b-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bd72b-124">INPUTS</span></span>

### <span data-ttu-id="bd72b-125">System. String</span><span class="sxs-lookup"><span data-stu-id="bd72b-125">System.String</span></span>

## <span data-ttu-id="bd72b-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bd72b-126">OUTPUTS</span></span>

### <span data-ttu-id="bd72b-127">Microsoft. Azure. Networking. ApplicationGatewayObjectModel. ApplicationGatewayConfigContext</span><span class="sxs-lookup"><span data-stu-id="bd72b-127">Microsoft.Azure.Networking.ApplicationGatewayObjectModel.ApplicationGatewayConfigContext</span></span>

## <span data-ttu-id="bd72b-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bd72b-128">NOTES</span></span>

## <span data-ttu-id="bd72b-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bd72b-129">RELATED LINKS</span></span>

[<span data-ttu-id="bd72b-130">Set-AzureApplicationGatewayConfig</span><span class="sxs-lookup"><span data-stu-id="bd72b-130">Set-AzureApplicationGatewayConfig</span></span>](./Set-AzureApplicationGatewayConfig.md)


