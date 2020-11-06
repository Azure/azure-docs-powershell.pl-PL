---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementbackendproxy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendProxy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendProxy.md
ms.openlocfilehash: 890f169c3fd497f7045522133e1e9e1f1d509aca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553711"
---
# <span data-ttu-id="dee9e-101">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="dee9e-101">New-AzureRmApiManagementBackendProxy</span></span>

## <span data-ttu-id="dee9e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dee9e-102">SYNOPSIS</span></span>
<span data-ttu-id="dee9e-103">Tworzy nowy obiekt pośredniczący zaplecza.</span><span class="sxs-lookup"><span data-stu-id="dee9e-103">Creates a new Backend Proxy Object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dee9e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dee9e-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackendProxy -Url <String> [-ProxyCredential <PSCredential>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dee9e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="dee9e-105">DESCRIPTION</span></span>
<span data-ttu-id="dee9e-106">Tworzy nowy obiekt pośredniczący zaplecza, który może zostać potokiem podczas tworzenia nowej jednostki wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="dee9e-106">Creates a new Backend Proxy Object which can be piped when creating a new Backend entity.</span></span>

## <span data-ttu-id="dee9e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dee9e-107">EXAMPLES</span></span>

### <span data-ttu-id="dee9e-108">Tworzenie obiektu pośredniczącego w wewnętrznej bazie danych In-Memory</span><span class="sxs-lookup"><span data-stu-id="dee9e-108">Create a Backend Proxy In-Memory Object</span></span>
```
PS C:\>$secpassword = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\>$proxyCreds = New-Object System.Management.Automation.PSCredential ("foo", $secpassword)
PS C:\>$credential = New-AzureRmApiManagementBackendProxy -Url "http://12.168.1.1:8080" -ProxyCredential $proxyCreds
```

<span data-ttu-id="dee9e-109">Tworzy obiekt pośredniczący zaplecza</span><span class="sxs-lookup"><span data-stu-id="dee9e-109">Creates a Backend Proxy Object</span></span>

## <span data-ttu-id="dee9e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dee9e-110">PARAMETERS</span></span>

### <span data-ttu-id="dee9e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dee9e-111">-DefaultProfile</span></span>
<span data-ttu-id="dee9e-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dee9e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dee9e-113">-ProxyCredential</span><span class="sxs-lookup"><span data-stu-id="dee9e-113">-ProxyCredential</span></span>
<span data-ttu-id="dee9e-114">Poświadczenia służące do nawiązywania połączenia z serwerem proxy zaplecza.</span><span class="sxs-lookup"><span data-stu-id="dee9e-114">Credentials used to connect to Backend Proxy.</span></span> <span data-ttu-id="dee9e-115">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="dee9e-115">This parameter is optional.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dee9e-116">-URL</span><span class="sxs-lookup"><span data-stu-id="dee9e-116">-Url</span></span>
<span data-ttu-id="dee9e-117">Adres URL serwera proxy, który ma być używany podczas przekierowywania połączeń do zaplecza.</span><span class="sxs-lookup"><span data-stu-id="dee9e-117">Url of the Proxy server to be used when forwarding calls to Backend.</span></span>
<span data-ttu-id="dee9e-118">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="dee9e-118">This parameter is required.</span></span>

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

### <span data-ttu-id="dee9e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dee9e-119">CommonParameters</span></span>
<span data-ttu-id="dee9e-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dee9e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dee9e-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dee9e-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dee9e-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dee9e-122">INPUTS</span></span>

### <span data-ttu-id="dee9e-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="dee9e-123">None</span></span>
<span data-ttu-id="dee9e-124">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="dee9e-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="dee9e-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dee9e-125">OUTPUTS</span></span>

### <span data-ttu-id="dee9e-126">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="dee9e-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

## <span data-ttu-id="dee9e-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dee9e-127">NOTES</span></span>

## <span data-ttu-id="dee9e-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dee9e-128">RELATED LINKS</span></span>

[<span data-ttu-id="dee9e-129">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="dee9e-129">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="dee9e-130">Nowe — AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="dee9e-130">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="dee9e-131">Nowe — AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="dee9e-131">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="dee9e-132">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="dee9e-132">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="dee9e-133">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="dee9e-133">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
