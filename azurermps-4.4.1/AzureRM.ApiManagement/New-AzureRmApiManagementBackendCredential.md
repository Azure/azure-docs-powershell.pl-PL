---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendCredential.md
ms.openlocfilehash: 58f80b6ff1742bfc6360844648d6ad18d12d8389
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547223"
---
# <span data-ttu-id="85b58-101">New-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="85b58-101">New-AzureRmApiManagementBackendCredential</span></span>

## <span data-ttu-id="85b58-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="85b58-102">SYNOPSIS</span></span>
<span data-ttu-id="85b58-103">Tworzy nowy kontrakt poświadczeń zaplecza.</span><span class="sxs-lookup"><span data-stu-id="85b58-103">Creates a new Backend Credential contract.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="85b58-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="85b58-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackendCredential [-CertificateThumbprint <String[]>] [-Query <Hashtable>]
 [-Header <Hashtable>] [-AuthorizationHeaderScheme <String>] [-AuthorizationHeaderParameter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="85b58-105">Opis</span><span class="sxs-lookup"><span data-stu-id="85b58-105">DESCRIPTION</span></span>
<span data-ttu-id="85b58-106">Tworzy nowy kontrakt poświadczeń zaplecza.</span><span class="sxs-lookup"><span data-stu-id="85b58-106">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="85b58-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="85b58-107">EXAMPLES</span></span>

### <span data-ttu-id="85b58-108">Tworzenie poświadczeń zaplecza In-Memory obiektu</span><span class="sxs-lookup"><span data-stu-id="85b58-108">Create a Backend Credentials In-Memory Object</span></span>
```
$credential = New-AzureRmApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}
```

<span data-ttu-id="85b58-109">Tworzenie kontraktu poświadczeń zaplecza</span><span class="sxs-lookup"><span data-stu-id="85b58-109">Creates a Backend Credentials Contract</span></span>

## <span data-ttu-id="85b58-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="85b58-110">PARAMETERS</span></span>

### <span data-ttu-id="85b58-111">-AuthorizationHeaderParameter</span><span class="sxs-lookup"><span data-stu-id="85b58-111">-AuthorizationHeaderParameter</span></span>
<span data-ttu-id="85b58-112">Nagłówek autoryzacji dla wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="85b58-112">Authorization Header used for the Backend.</span></span>
<span data-ttu-id="85b58-113">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="85b58-113">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85b58-114">-AuthorizationHeaderScheme</span><span class="sxs-lookup"><span data-stu-id="85b58-114">-AuthorizationHeaderScheme</span></span>
<span data-ttu-id="85b58-115">Schemat autoryzacji stosowany w wewnętrznej bazie danych.</span><span class="sxs-lookup"><span data-stu-id="85b58-115">Authorization Scheme used for the Backend.</span></span>
<span data-ttu-id="85b58-116">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="85b58-116">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85b58-117">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="85b58-117">-CertificateThumbprint</span></span>
<span data-ttu-id="85b58-118">Odciski palców certyfikatu klienta.</span><span class="sxs-lookup"><span data-stu-id="85b58-118">Client Certificate Thumbprints.</span></span>
<span data-ttu-id="85b58-119">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="85b58-119">This parameter is optional.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85b58-120">-Header</span><span class="sxs-lookup"><span data-stu-id="85b58-120">-Header</span></span>
<span data-ttu-id="85b58-121">Wartości parametru nagłówka zaakceptowane przez zaplecze.</span><span class="sxs-lookup"><span data-stu-id="85b58-121">Header Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="85b58-122">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="85b58-122">This parameter is optional.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85b58-123">-Query</span><span class="sxs-lookup"><span data-stu-id="85b58-123">-Query</span></span>
<span data-ttu-id="85b58-124">Wartości parametrów kwerendy zaakceptowane przez zaplecze.</span><span class="sxs-lookup"><span data-stu-id="85b58-124">Query Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="85b58-125">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="85b58-125">This parameter is optional.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85b58-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85b58-126">-DefaultProfile</span></span>
<span data-ttu-id="85b58-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="85b58-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85b58-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85b58-128">CommonParameters</span></span>
<span data-ttu-id="85b58-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85b58-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85b58-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85b58-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85b58-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="85b58-131">INPUTS</span></span>

## <span data-ttu-id="85b58-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="85b58-132">OUTPUTS</span></span>

### <span data-ttu-id="85b58-133">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="85b58-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

## <span data-ttu-id="85b58-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="85b58-134">NOTES</span></span>

## <span data-ttu-id="85b58-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="85b58-135">RELATED LINKS</span></span>

[<span data-ttu-id="85b58-136">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="85b58-136">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="85b58-137">Nowe — AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="85b58-137">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="85b58-138">Nowe — AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="85b58-138">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="85b58-139">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="85b58-139">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="85b58-140">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="85b58-140">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
