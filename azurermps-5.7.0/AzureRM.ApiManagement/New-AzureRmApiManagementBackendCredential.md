---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementbackendcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendCredential.md
ms.openlocfilehash: 4453b7fc3e13f4de2632c41cea966fdada1d84f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553712"
---
# <span data-ttu-id="15232-101">New-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="15232-101">New-AzureRmApiManagementBackendCredential</span></span>

## <span data-ttu-id="15232-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="15232-102">SYNOPSIS</span></span>
<span data-ttu-id="15232-103">Tworzy nowy kontrakt poświadczeń zaplecza.</span><span class="sxs-lookup"><span data-stu-id="15232-103">Creates a new Backend Credential contract.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="15232-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="15232-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackendCredential [-CertificateThumbprint <String[]>] [-Query <Hashtable>]
 [-Header <Hashtable>] [-AuthorizationHeaderScheme <String>] [-AuthorizationHeaderParameter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15232-105">Opis</span><span class="sxs-lookup"><span data-stu-id="15232-105">DESCRIPTION</span></span>
<span data-ttu-id="15232-106">Tworzy nowy kontrakt poświadczeń zaplecza.</span><span class="sxs-lookup"><span data-stu-id="15232-106">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="15232-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="15232-107">EXAMPLES</span></span>

### <span data-ttu-id="15232-108">Tworzenie poświadczeń zaplecza In-Memory obiektu</span><span class="sxs-lookup"><span data-stu-id="15232-108">Create a Backend Credentials In-Memory Object</span></span>
```
PS C:\>$credential = New-AzureRmApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}
```

<span data-ttu-id="15232-109">Tworzenie kontraktu poświadczeń zaplecza</span><span class="sxs-lookup"><span data-stu-id="15232-109">Creates a Backend Credentials Contract</span></span>

## <span data-ttu-id="15232-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="15232-110">PARAMETERS</span></span>

### <span data-ttu-id="15232-111">-AuthorizationHeaderParameter</span><span class="sxs-lookup"><span data-stu-id="15232-111">-AuthorizationHeaderParameter</span></span>
<span data-ttu-id="15232-112">Nagłówek autoryzacji dla wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="15232-112">Authorization Header used for the Backend.</span></span>
<span data-ttu-id="15232-113">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="15232-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="15232-114">-AuthorizationHeaderScheme</span><span class="sxs-lookup"><span data-stu-id="15232-114">-AuthorizationHeaderScheme</span></span>
<span data-ttu-id="15232-115">Schemat autoryzacji stosowany w wewnętrznej bazie danych.</span><span class="sxs-lookup"><span data-stu-id="15232-115">Authorization Scheme used for the Backend.</span></span>
<span data-ttu-id="15232-116">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="15232-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="15232-117">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="15232-117">-CertificateThumbprint</span></span>
<span data-ttu-id="15232-118">Odciski palców certyfikatu klienta.</span><span class="sxs-lookup"><span data-stu-id="15232-118">Client Certificate Thumbprints.</span></span>
<span data-ttu-id="15232-119">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="15232-119">This parameter is optional.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15232-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15232-120">-DefaultProfile</span></span>
<span data-ttu-id="15232-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="15232-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="15232-122">-Header</span><span class="sxs-lookup"><span data-stu-id="15232-122">-Header</span></span>
<span data-ttu-id="15232-123">Wartości parametru nagłówka zaakceptowane przez zaplecze.</span><span class="sxs-lookup"><span data-stu-id="15232-123">Header Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="15232-124">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="15232-124">This parameter is optional.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15232-125">-Query</span><span class="sxs-lookup"><span data-stu-id="15232-125">-Query</span></span>
<span data-ttu-id="15232-126">Wartości parametrów kwerendy zaakceptowane przez zaplecze.</span><span class="sxs-lookup"><span data-stu-id="15232-126">Query Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="15232-127">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="15232-127">This parameter is optional.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15232-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15232-128">CommonParameters</span></span>
<span data-ttu-id="15232-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15232-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15232-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15232-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15232-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="15232-131">INPUTS</span></span>

### <span data-ttu-id="15232-132">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="15232-132">None</span></span>
<span data-ttu-id="15232-133">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="15232-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="15232-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="15232-134">OUTPUTS</span></span>

### <span data-ttu-id="15232-135">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="15232-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

## <span data-ttu-id="15232-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="15232-136">NOTES</span></span>

## <span data-ttu-id="15232-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="15232-137">RELATED LINKS</span></span>

[<span data-ttu-id="15232-138">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="15232-138">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="15232-139">Nowe — AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="15232-139">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="15232-140">Nowe — AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="15232-140">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="15232-141">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="15232-141">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="15232-142">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="15232-142">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
