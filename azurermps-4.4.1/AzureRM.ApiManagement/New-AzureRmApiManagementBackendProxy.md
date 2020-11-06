---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendProxy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendProxy.md
ms.openlocfilehash: d3699347d21f17452d521afb3bc5524f8e68e40b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547215"
---
# <span data-ttu-id="99cf5-101">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="99cf5-101">New-AzureRmApiManagementBackendProxy</span></span>

## <span data-ttu-id="99cf5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="99cf5-102">SYNOPSIS</span></span>
<span data-ttu-id="99cf5-103">Tworzy nowy obiekt pośredniczący zaplecza.</span><span class="sxs-lookup"><span data-stu-id="99cf5-103">Creates a new Backend Proxy Object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99cf5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="99cf5-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackendProxy -Url <String> [-UserName <String>] [-Password <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99cf5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="99cf5-105">DESCRIPTION</span></span>
<span data-ttu-id="99cf5-106">Tworzy nowy obiekt pośredniczący zaplecza, który może zostać potokiem podczas tworzenia nowej jednostki wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="99cf5-106">Creates a new Backend Proxy Object which can be piped when creating a new Backend entity.</span></span>

## <span data-ttu-id="99cf5-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="99cf5-107">EXAMPLES</span></span>

### <span data-ttu-id="99cf5-108">Tworzenie obiektu pośredniczącego w wewnętrznej bazie danych In-Memory</span><span class="sxs-lookup"><span data-stu-id="99cf5-108">Create a Backend Proxy In-Memory Object</span></span>
```
$proxy= New-AzureRmApiManagementBackendProxy -Url "https://abbc.def.g" -UserName "apim" -Password "password"
```

<span data-ttu-id="99cf5-109">Tworzy obiekt pośredniczący zaplecza</span><span class="sxs-lookup"><span data-stu-id="99cf5-109">Creates a Backend Proxy Object</span></span>

## <span data-ttu-id="99cf5-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="99cf5-110">PARAMETERS</span></span>

### <span data-ttu-id="99cf5-111">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="99cf5-111">-Password</span></span>
<span data-ttu-id="99cf5-112">Hasło serwera proxy używane w celu nawiązania połączenia z serwerem proxy zaplecza.</span><span class="sxs-lookup"><span data-stu-id="99cf5-112">Proxy Password used to connect to Backend Proxy.</span></span>
<span data-ttu-id="99cf5-113">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="99cf5-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="99cf5-114">-URL</span><span class="sxs-lookup"><span data-stu-id="99cf5-114">-Url</span></span>
<span data-ttu-id="99cf5-115">Adres URL serwera proxy, który ma być używany podczas przekierowywania połączeń do zaplecza.</span><span class="sxs-lookup"><span data-stu-id="99cf5-115">Url of the Proxy server to be used when forwarding calls to Backend.</span></span>
<span data-ttu-id="99cf5-116">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="99cf5-116">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99cf5-117">-UserName</span><span class="sxs-lookup"><span data-stu-id="99cf5-117">-UserName</span></span>
<span data-ttu-id="99cf5-118">Nazwa użytkownika serwera proxy używana do nawiązywania połączenia z serwerem proxy zaplecza.</span><span class="sxs-lookup"><span data-stu-id="99cf5-118">Proxy UserName used to connect to Backend Proxy.</span></span>
<span data-ttu-id="99cf5-119">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="99cf5-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="99cf5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99cf5-120">-DefaultProfile</span></span>
<span data-ttu-id="99cf5-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="99cf5-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99cf5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99cf5-122">CommonParameters</span></span>
<span data-ttu-id="99cf5-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99cf5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99cf5-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99cf5-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99cf5-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="99cf5-125">INPUTS</span></span>

## <span data-ttu-id="99cf5-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="99cf5-126">OUTPUTS</span></span>

### <span data-ttu-id="99cf5-127">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="99cf5-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

## <span data-ttu-id="99cf5-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="99cf5-128">NOTES</span></span>

## <span data-ttu-id="99cf5-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="99cf5-129">RELATED LINKS</span></span>

[<span data-ttu-id="99cf5-130">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="99cf5-130">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="99cf5-131">Nowe — AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="99cf5-131">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="99cf5-132">Nowe — AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="99cf5-132">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="99cf5-133">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="99cf5-133">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="99cf5-134">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="99cf5-134">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
