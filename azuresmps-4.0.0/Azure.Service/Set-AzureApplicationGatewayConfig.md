---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: D7D99AFA-A85E-43DA-9F2F-8FFD34048E00
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7ede675ab58905f102fb9d0029669115acdb9e85
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055395"
---
# <span data-ttu-id="9850e-101">Set-AzureApplicationGatewayConfig</span><span class="sxs-lookup"><span data-stu-id="9850e-101">Set-AzureApplicationGatewayConfig</span></span>

## <span data-ttu-id="9850e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9850e-102">SYNOPSIS</span></span>
<span data-ttu-id="9850e-103">Konfiguruje bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="9850e-103">Configures an application gateway.</span></span>

## <span data-ttu-id="9850e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9850e-104">SYNTAX</span></span>

### <span data-ttu-id="9850e-105">configFile</span><span class="sxs-lookup"><span data-stu-id="9850e-105">configFile</span></span>
```
Set-AzureApplicationGatewayConfig -Name <String> -ConfigFile <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="9850e-106">configObject</span><span class="sxs-lookup"><span data-stu-id="9850e-106">configObject</span></span>
```
Set-AzureApplicationGatewayConfig -Name <String> -Config <ApplicationGatewayConfiguration>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9850e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="9850e-107">DESCRIPTION</span></span>
<span data-ttu-id="9850e-108">Polecenie cmdlet **Set-AzureApplicationGatewayConfig** konfiguruje bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="9850e-108">The **Set-AzureApplicationGatewayConfig** cmdlet configures an application gateway.</span></span>

## <span data-ttu-id="9850e-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9850e-109">EXAMPLES</span></span>

### <span data-ttu-id="9850e-110">Przykład 1: Konfigurowanie bramy aplikacji przy użyciu obiektu konfiguracji</span><span class="sxs-lookup"><span data-stu-id="9850e-110">Example 1: Configure an application gateway by using a configuration object</span></span>
```
PS C:\> $ConfigReturnObject = Get-AzureApplicationGatewayConfig -Name "ApplicationGateway02"
PS C:\> Set-AzureApplicationGatewayConfig -Name "ApplicationGateway06" -Config $ConfigReturnObject
```

<span data-ttu-id="9850e-111">Pierwsze polecenie pobiera obiekt konfiguracji bramy Application Gateway o nazwie ApplicationGateway02 przy użyciu polecenia cmdlet **Get-AzureApplicationGatewayConfig** .</span><span class="sxs-lookup"><span data-stu-id="9850e-111">The first command gets the configuration object for the application gateway named ApplicationGateway02 by using the **Get-AzureApplicationGatewayConfig** cmdlet.</span></span>
<span data-ttu-id="9850e-112">Polecenie zapisuje je w zmiennej $ConfigReturnObject.</span><span class="sxs-lookup"><span data-stu-id="9850e-112">The command stores it in the $ConfigReturnObject variable.</span></span>

<span data-ttu-id="9850e-113">Drugie polecenie ustawia konfigurację dla aplikacji o nazwie ApplicationGateway06 przy użyciu obiektu konfiguracji bramy aplikacji przechowywanego w zmiennej $ConfigReturnObject.</span><span class="sxs-lookup"><span data-stu-id="9850e-113">The second command sets the configuration for the application named ApplicationGateway06 by using an application gateway configuration object stored in the $ConfigReturnObject variable.</span></span>

### <span data-ttu-id="9850e-114">Przykład 2: Konfigurowanie bramy aplikacji przy użyciu pliku konfiguracji</span><span class="sxs-lookup"><span data-stu-id="9850e-114">Example 2: Configure an application gateway by using a configuration file</span></span>
```
PS C:\> Set-AzureApplicationGatewayConfig -Name "ApplicationGateway06" -ConfigFile "D:\config.xml"
```

<span data-ttu-id="9850e-115">To polecenie ustawia konfigurację dla aplikacji o nazwie ApplicationGateway06 przy użyciu pliku konfiguracji bramy aplikacji w określonej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="9850e-115">This command sets the configuration for the application named ApplicationGateway06 by using an application gateway configuration file in the specified location.</span></span>

### <span data-ttu-id="9850e-116">Przykład 3: modyfikowanie konfiguracji przy użyciu obiektu konfiguracji</span><span class="sxs-lookup"><span data-stu-id="9850e-116">Example 3: Modify a configuration by using a configuration object</span></span>
```
PS C:\> $ConfigReturnObject = Get-AzureApplicationGatewayConfig -Name "ApplicationGateway06"
PS C:\> $ConfigReturnObject.Config.FrontendPorts[0].Port = 443
PS C:\> $ConfigReturnObject | Set-AzureApplicationGatewayConfig -Name "ApplicationGateway06"
```

<span data-ttu-id="9850e-117">Pierwsze polecenie pobiera obiekt konfiguracji bramy Application Gateway o nazwie ApplicationGateway06 przy użyciu polecenia cmdlet **Get-AzureApplicationGatewayConfig** .</span><span class="sxs-lookup"><span data-stu-id="9850e-117">The first command gets the configuration object for the application gateway named ApplicationGateway06 by using the **Get-AzureApplicationGatewayConfig** cmdlet.</span></span>
<span data-ttu-id="9850e-118">Polecenie zapisuje je w zmiennej $ConfigReturnObject.</span><span class="sxs-lookup"><span data-stu-id="9850e-118">The command stores it in the $ConfigReturnObject variable.</span></span>

<span data-ttu-id="9850e-119">Drugie polecenie przypisuje wartość portu do właściwości **port** w obiekcie przechowywanym w $ConfigReturnObject.</span><span class="sxs-lookup"><span data-stu-id="9850e-119">The second command assigns a port value to a **Port** property in the object stored in $ConfigReturnObject.</span></span>

<span data-ttu-id="9850e-120">Polecenie ostatnie przekazuje zaktualizowaną $ConfigReturnObject do bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9850e-120">The final command passes the updated $ConfigReturnObject to the current cmdlet.</span></span>

## <span data-ttu-id="9850e-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9850e-121">PARAMETERS</span></span>

### <span data-ttu-id="9850e-122">-Config</span><span class="sxs-lookup"><span data-stu-id="9850e-122">-Config</span></span>
<span data-ttu-id="9850e-123">Określa obiekt konfiguracji bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="9850e-123">Specifies an application gateway configuration object.</span></span>
<span data-ttu-id="9850e-124">To polecenie cmdlet umożliwia przypisanie konfiguracji, którą ten parametr określa do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="9850e-124">This cmdlet assigns the configuration that this parameter specifies to an application gateway.</span></span>

```yaml
Type: ApplicationGatewayConfiguration
Parameter Sets: configObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9850e-125">-ConfigFile</span><span class="sxs-lookup"><span data-stu-id="9850e-125">-ConfigFile</span></span>
<span data-ttu-id="9850e-126">Określa ścieżkę pliku konfiguracji w formacie XML dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="9850e-126">Specifies the path of a configuration file, in XML format, for an application gateway.</span></span>
<span data-ttu-id="9850e-127">To polecenie cmdlet umożliwia przypisanie konfiguracji, którą ten parametr określa do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="9850e-127">This cmdlet assigns the configuration that this parameter specifies to an application gateway.</span></span>

```yaml
Type: String
Parameter Sets: configFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9850e-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9850e-128">-Name</span></span>
<span data-ttu-id="9850e-129">Określa nazwę bramy aplikacji, którą konfiguruje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9850e-129">Specifies the name of the application gateway that this cmdlet configures.</span></span>

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

### <span data-ttu-id="9850e-130">-Profile</span><span class="sxs-lookup"><span data-stu-id="9850e-130">-Profile</span></span>
<span data-ttu-id="9850e-131">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9850e-131">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="9850e-132">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="9850e-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9850e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9850e-133">CommonParameters</span></span>
<span data-ttu-id="9850e-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9850e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9850e-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9850e-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9850e-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9850e-136">INPUTS</span></span>

### <span data-ttu-id="9850e-137">System. String, Microsoft. Azure. Networking. ApplicationGatewayObjectModel. ApplicationGatewayConfiguration</span><span class="sxs-lookup"><span data-stu-id="9850e-137">System.String, Microsoft.Azure.Networking.ApplicationGatewayObjectModel.ApplicationGatewayConfiguration</span></span>

## <span data-ttu-id="9850e-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9850e-138">OUTPUTS</span></span>

### <span data-ttu-id="9850e-139">Microsoft. platformy windowsazure. Management. ApplicationGateway. MODELES. ApplicationGatewayOperationResponse</span><span class="sxs-lookup"><span data-stu-id="9850e-139">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="9850e-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9850e-140">NOTES</span></span>

## <span data-ttu-id="9850e-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9850e-141">RELATED LINKS</span></span>

[<span data-ttu-id="9850e-142">Get-AzureApplicationGatewayConfig</span><span class="sxs-lookup"><span data-stu-id="9850e-142">Get-AzureApplicationGatewayConfig</span></span>](./Get-AzureApplicationGatewayConfig.md)


