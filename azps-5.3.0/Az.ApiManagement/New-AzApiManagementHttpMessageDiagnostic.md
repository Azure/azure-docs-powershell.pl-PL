---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementhttpmessagediagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementHttpMessageDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementHttpMessageDiagnostic.md
ms.openlocfilehash: 10c84654bb5d074ee9f668062d1fa7a18d92f8b0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502406"
---
# <span data-ttu-id="b8ec1-101">New-AzApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="b8ec1-101">New-AzApiManagementHttpMessageDiagnostic</span></span>

## <span data-ttu-id="b8ec1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b8ec1-102">SYNOPSIS</span></span>
<span data-ttu-id="b8ec1-103">Tworzy wystąpienie **PsApiManagementHttpMessageDiagnostic** , które jest ustawieniem diagnostycznym wiadomości HTTP w diagnostyce.</span><span class="sxs-lookup"><span data-stu-id="b8ec1-103">Creates an instance of **PsApiManagementHttpMessageDiagnostic** which is an Http Message diagnostic setting of the Diagnostic</span></span>

## <span data-ttu-id="b8ec1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b8ec1-104">SYNTAX</span></span>

```
New-AzApiManagementHttpMessageDiagnostic [-HeadersToLog <String[]>] [-BodyBytesToLog <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8ec1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b8ec1-105">DESCRIPTION</span></span>
<span data-ttu-id="b8ec1-106">Polecenie cmdlet **New-AzApiManagementHttpMessageDiagnostic** tworzy ustawienia diagnostyczne wiadomości HTTP.</span><span class="sxs-lookup"><span data-stu-id="b8ec1-106">The cmdlet **New-AzApiManagementHttpMessageDiagnostic** creates the Http Message diagnostic setting.</span></span>

## <span data-ttu-id="b8ec1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b8ec1-107">EXAMPLES</span></span>

### <span data-ttu-id="b8ec1-108">Przykład 1: Tworzenie podstawowego ustawienia diagnostycznego wiadomości http</span><span class="sxs-lookup"><span data-stu-id="b8ec1-108">Example 1: Create a Basic Http Message diagnostic Setting</span></span>
```powershell
PS C:\>  New-AzApiManagementHttpMessageDiagnostic -Headers 'Content-Type', 'UserAgent' -BodyBytes 100

Headers                   Body
-------                   ----
{Content-Type, UserAgent} Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBodyDiagnosticSetting
```

<span data-ttu-id="b8ec1-109">Tworzenie ustawienia diagnostycznego wiadomości HTTP do rejestrowania `Content-Type` i `User-Agent` nagłówków wraz z 100ą bajtów `body`</span><span class="sxs-lookup"><span data-stu-id="b8ec1-109">Create a http message diagnostic setting to log `Content-Type` and `User-Agent` headers along with 100 bytes of `body`</span></span>

## <span data-ttu-id="b8ec1-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b8ec1-110">PARAMETERS</span></span>

### <span data-ttu-id="b8ec1-111">-BodyBytesToLog</span><span class="sxs-lookup"><span data-stu-id="b8ec1-111">-BodyBytesToLog</span></span>
<span data-ttu-id="b8ec1-112">Liczba bajtów treści żądania do zarejestrowania.</span><span class="sxs-lookup"><span data-stu-id="b8ec1-112">Number of request body bytes to log.</span></span> <span data-ttu-id="b8ec1-113">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="b8ec1-113">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8ec1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8ec1-114">-DefaultProfile</span></span>
<span data-ttu-id="b8ec1-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b8ec1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8ec1-116">-HeadersToLog</span><span class="sxs-lookup"><span data-stu-id="b8ec1-116">-HeadersToLog</span></span>
<span data-ttu-id="b8ec1-117">Tablica nagłówków, które mają zostać zarejestrowane.</span><span class="sxs-lookup"><span data-stu-id="b8ec1-117">The array of headers to log.</span></span> <span data-ttu-id="b8ec1-118">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="b8ec1-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="b8ec1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8ec1-119">CommonParameters</span></span>
<span data-ttu-id="b8ec1-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8ec1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8ec1-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b8ec1-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8ec1-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b8ec1-122">INPUTS</span></span>

### <span data-ttu-id="b8ec1-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="b8ec1-123">None</span></span>

## <span data-ttu-id="b8ec1-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b8ec1-124">OUTPUTS</span></span>

### <span data-ttu-id="b8ec1-125">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="b8ec1-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic</span></span>

## <span data-ttu-id="b8ec1-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b8ec1-126">NOTES</span></span>

## <span data-ttu-id="b8ec1-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b8ec1-127">RELATED LINKS</span></span>

[<span data-ttu-id="b8ec1-128">Nowe — AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="b8ec1-128">New-AzApiManagementDiagnostic</span></span>](./New-AzApiManagementDiagnostic.md)

[<span data-ttu-id="b8ec1-129">Nowe — AzApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="b8ec1-129">New-AzApiManagementSamplingSetting</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)