---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackendcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendCredential.md
ms.openlocfilehash: 2cde898622c870dc0598639addb1e8b30e438076
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707027"
---
# <span data-ttu-id="e3008-101">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="e3008-101">New-AzApiManagementBackendCredential</span></span>

## <span data-ttu-id="e3008-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e3008-102">SYNOPSIS</span></span>
<span data-ttu-id="e3008-103">Tworzy nowy kontrakt poświadczeń zaplecza.</span><span class="sxs-lookup"><span data-stu-id="e3008-103">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="e3008-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e3008-104">SYNTAX</span></span>

```
New-AzApiManagementBackendCredential [-CertificateThumbprint <String[]>] [-Query <Hashtable>]
 [-Header <Hashtable>] [-AuthorizationHeaderScheme <String>] [-AuthorizationHeaderParameter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3008-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e3008-105">DESCRIPTION</span></span>
<span data-ttu-id="e3008-106">Tworzy nowy kontrakt poświadczeń zaplecza.</span><span class="sxs-lookup"><span data-stu-id="e3008-106">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="e3008-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e3008-107">EXAMPLES</span></span>

### <span data-ttu-id="e3008-108">Tworzenie poświadczeń zaplecza In-Memory obiektu</span><span class="sxs-lookup"><span data-stu-id="e3008-108">Create a Backend Credentials In-Memory Object</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="e3008-109">Tworzenie kontraktu poświadczeń zaplecza</span><span class="sxs-lookup"><span data-stu-id="e3008-109">Creates a Backend Credentials Contract</span></span>

## <span data-ttu-id="e3008-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e3008-110">PARAMETERS</span></span>

### <span data-ttu-id="e3008-111">-AuthorizationHeaderParameter</span><span class="sxs-lookup"><span data-stu-id="e3008-111">-AuthorizationHeaderParameter</span></span>
<span data-ttu-id="e3008-112">Nagłówek autoryzacji dla wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="e3008-112">Authorization Header used for the Backend.</span></span>
<span data-ttu-id="e3008-113">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="e3008-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="e3008-114">-AuthorizationHeaderScheme</span><span class="sxs-lookup"><span data-stu-id="e3008-114">-AuthorizationHeaderScheme</span></span>
<span data-ttu-id="e3008-115">Schemat autoryzacji stosowany w wewnętrznej bazie danych.</span><span class="sxs-lookup"><span data-stu-id="e3008-115">Authorization Scheme used for the Backend.</span></span>
<span data-ttu-id="e3008-116">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="e3008-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="e3008-117">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="e3008-117">-CertificateThumbprint</span></span>
<span data-ttu-id="e3008-118">Odciski palców certyfikatu klienta.</span><span class="sxs-lookup"><span data-stu-id="e3008-118">Client Certificate Thumbprints.</span></span>
<span data-ttu-id="e3008-119">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="e3008-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="e3008-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3008-120">-DefaultProfile</span></span>
<span data-ttu-id="e3008-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e3008-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3008-122">-Header</span><span class="sxs-lookup"><span data-stu-id="e3008-122">-Header</span></span>
<span data-ttu-id="e3008-123">Wartości parametru nagłówka zaakceptowane przez zaplecze.</span><span class="sxs-lookup"><span data-stu-id="e3008-123">Header Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="e3008-124">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="e3008-124">This parameter is optional.</span></span>

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

### <span data-ttu-id="e3008-125">-Query</span><span class="sxs-lookup"><span data-stu-id="e3008-125">-Query</span></span>
<span data-ttu-id="e3008-126">Wartości parametrów kwerendy zaakceptowane przez zaplecze.</span><span class="sxs-lookup"><span data-stu-id="e3008-126">Query Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="e3008-127">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="e3008-127">This parameter is optional.</span></span>

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

### <span data-ttu-id="e3008-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3008-128">CommonParameters</span></span>
<span data-ttu-id="e3008-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3008-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3008-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e3008-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3008-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e3008-131">INPUTS</span></span>

### <span data-ttu-id="e3008-132">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="e3008-132">None</span></span>

## <span data-ttu-id="e3008-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e3008-133">OUTPUTS</span></span>

### <span data-ttu-id="e3008-134">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="e3008-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

## <span data-ttu-id="e3008-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e3008-135">NOTES</span></span>

## <span data-ttu-id="e3008-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e3008-136">RELATED LINKS</span></span>

[<span data-ttu-id="e3008-137">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e3008-137">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend)

[<span data-ttu-id="e3008-138">Nowe — AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e3008-138">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="e3008-139">Nowe — AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="e3008-139">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="e3008-140">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e3008-140">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="e3008-141">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e3008-141">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
