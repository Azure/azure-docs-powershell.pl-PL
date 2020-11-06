---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5B4ADD38-FA22-4C25-9B9C-FD7861883811
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementLogger.md
ms.openlocfilehash: c21c227dd748f28523f4ac616d003e029d19e38f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548431"
---
# <span data-ttu-id="c61a0-101">Set-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="c61a0-101">Set-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="c61a0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c61a0-102">SYNOPSIS</span></span>
<span data-ttu-id="c61a0-103">Modyfikuje rejestratora zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="c61a0-103">Modifies an API Management Logger.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c61a0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c61a0-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-Name <String>]
 [-ConnectionString <String>] [-Description <String>] [-IsBuffered] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c61a0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c61a0-105">DESCRIPTION</span></span>
<span data-ttu-id="c61a0-106">Polecenie cmdlet **Set-AzureRmApiManagementLogger** modyfikuje ustawienia **rejestratora** zarządzania interfejsem Azure API.</span><span class="sxs-lookup"><span data-stu-id="c61a0-106">The **Set-AzureRmApiManagementLogger** cmdlet modifies settings of an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="c61a0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c61a0-107">EXAMPLES</span></span>

### <span data-ttu-id="c61a0-108">Przykład 1: modyfikowanie rejestratora</span><span class="sxs-lookup"><span data-stu-id="c61a0-108">Example 1: Modify a logger</span></span>
```
PS C:\>Set-AzureRmApiManagementLogger -Context $ApimContext -LoggerId "Logger123" -Name "ContosoSdkEventHub" -ConnectionString "Endpoint=sb://ContosoSdkEventHubs.servicebus.windows.net/;SharedAccessKeyName=SendKey;SharedAccessKey=<key>" -Description "updated SDK event hub logger" -PassThru
```

<span data-ttu-id="c61a0-109">To polecenie modyfikuje rejestratora o IDENTYFIKATORze Logger123.</span><span class="sxs-lookup"><span data-stu-id="c61a0-109">This command modifies a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="c61a0-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c61a0-110">PARAMETERS</span></span>

### <span data-ttu-id="c61a0-111">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="c61a0-111">-ConnectionString</span></span>
<span data-ttu-id="c61a0-112">Określa parametry połączenia z koncentratorem zdarzeń platformy Azure, które zawiera prawa do wysyłania.</span><span class="sxs-lookup"><span data-stu-id="c61a0-112">Specifies an Azure Event Hubs connection string that includes Send policy rights.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c61a0-113">-Context</span><span class="sxs-lookup"><span data-stu-id="c61a0-113">-Context</span></span>
<span data-ttu-id="c61a0-114">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="c61a0-114">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c61a0-115">— Opis</span><span class="sxs-lookup"><span data-stu-id="c61a0-115">-Description</span></span>
<span data-ttu-id="c61a0-116">Określa opis.</span><span class="sxs-lookup"><span data-stu-id="c61a0-116">Specifies a description.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c61a0-117">-IsBuffered</span><span class="sxs-lookup"><span data-stu-id="c61a0-117">-IsBuffered</span></span>
<span data-ttu-id="c61a0-118">Określa, że rekordy w rejestratorze są buforowane przed opublikowaniem.</span><span class="sxs-lookup"><span data-stu-id="c61a0-118">Specifies that the records in the logger are buffered before publishing.</span></span>
<span data-ttu-id="c61a0-119">Gdy rekordy są buforowane, są one wysyłane do koncentratorów zdarzeń co 15 sekund lub za każdym razem, gdy bufor otrzymuje 256 KB wiadomości.</span><span class="sxs-lookup"><span data-stu-id="c61a0-119">When records are buffered, they are sent to Event Hubs every 15 seconds, or whenever the buffer receives 256 KB of messages.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c61a0-120">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="c61a0-120">-LoggerId</span></span>
<span data-ttu-id="c61a0-121">Określa identyfikator rejestratora do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="c61a0-121">Specifies the ID of the logger to update.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c61a0-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c61a0-122">-Name</span></span>
<span data-ttu-id="c61a0-123">Określa nazwę encji centrum zdarzeń w portalu klasycznym usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="c61a0-123">Specifies the entity name of an event hub from Azure classic portal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c61a0-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c61a0-124">-PassThru</span></span>
<span data-ttu-id="c61a0-125">Wskazuje, że to polecenie cmdlet zwróci  **PsApiManagementLogger** , które modyfikuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c61a0-125">Indicates that this cmdlet returns the  **PsApiManagementLogger** that this cmdlet modifies.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c61a0-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c61a0-126">-DefaultProfile</span></span>
<span data-ttu-id="c61a0-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c61a0-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c61a0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c61a0-128">CommonParameters</span></span>
<span data-ttu-id="c61a0-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c61a0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c61a0-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c61a0-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c61a0-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c61a0-131">INPUTS</span></span>

## <span data-ttu-id="c61a0-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c61a0-132">OUTPUTS</span></span>

### <span data-ttu-id="c61a0-133">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="c61a0-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="c61a0-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c61a0-134">NOTES</span></span>

## <span data-ttu-id="c61a0-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c61a0-135">RELATED LINKS</span></span>

[<span data-ttu-id="c61a0-136">Get-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="c61a0-136">Get-AzureRmApiManagementLogger</span></span>](./Get-AzureRmApiManagementLogger.md)

[<span data-ttu-id="c61a0-137">Nowe — AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="c61a0-137">New-AzureRmApiManagementLogger</span></span>](./New-AzureRmApiManagementLogger.md)

[<span data-ttu-id="c61a0-138">Remove-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="c61a0-138">Remove-AzureRmApiManagementLogger</span></span>](./Remove-AzureRmApiManagementLogger.md)


