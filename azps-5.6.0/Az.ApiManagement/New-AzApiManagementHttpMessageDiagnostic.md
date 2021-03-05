---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementhttpmessagediagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementHttpMessageDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementHttpMessageDiagnostic.md
ms.openlocfilehash: 3475778104655e6b27061edf08ced376f192ea34
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988541"
---
# <span data-ttu-id="76ddf-101">New-AzApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="76ddf-101">New-AzApiManagementHttpMessageDiagnostic</span></span>

## <span data-ttu-id="76ddf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76ddf-102">SYNOPSIS</span></span>
<span data-ttu-id="76ddf-103">Tworzy wystąpienie narzędzia **PsApiManagementHttpMessageDiagnostic,** które jest ustawieniem diagnostycznym Http Message narzędzia Diagnostic</span><span class="sxs-lookup"><span data-stu-id="76ddf-103">Creates an instance of **PsApiManagementHttpMessageDiagnostic** which is an Http Message diagnostic setting of the Diagnostic</span></span>

## <span data-ttu-id="76ddf-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="76ddf-104">SYNTAX</span></span>

```
New-AzApiManagementHttpMessageDiagnostic [-HeadersToLog <String[]>] [-BodyBytesToLog <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76ddf-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="76ddf-105">DESCRIPTION</span></span>
<span data-ttu-id="76ddf-106">Polecenie cmdlet **New-AzApiManagementHttpMessageDiagnostic** tworzy ustawienie diagnostyczne http wiadomości.</span><span class="sxs-lookup"><span data-stu-id="76ddf-106">The cmdlet **New-AzApiManagementHttpMessageDiagnostic** creates the Http Message diagnostic setting.</span></span>

## <span data-ttu-id="76ddf-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="76ddf-107">EXAMPLES</span></span>

### <span data-ttu-id="76ddf-108">Przykład 1. Tworzenie podstawowego ustawienia diagnostycznego wiadomości HTTP</span><span class="sxs-lookup"><span data-stu-id="76ddf-108">Example 1: Create a Basic Http Message diagnostic Setting</span></span>
```powershell
PS C:\>  New-AzApiManagementHttpMessageDiagnostic -Headers 'Content-Type', 'UserAgent' -BodyBytes 100

Headers                   Body
-------                   ----
{Content-Type, UserAgent} Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBodyDiagnosticSetting
```

<span data-ttu-id="76ddf-109">Tworzenie ustawienia diagnostycznego wiadomości HTTP do dziennika `Content-Type` i `User-Agent` nagłówków wraz z 100 bajtami `body`</span><span class="sxs-lookup"><span data-stu-id="76ddf-109">Create a http message diagnostic setting to log `Content-Type` and `User-Agent` headers along with 100 bytes of `body`</span></span>

## <span data-ttu-id="76ddf-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="76ddf-110">PARAMETERS</span></span>

### <span data-ttu-id="76ddf-111">-BodyBytesToLog</span><span class="sxs-lookup"><span data-stu-id="76ddf-111">-BodyBytesToLog</span></span>
<span data-ttu-id="76ddf-112">Liczba bajtów treści żądania do dziennika.</span><span class="sxs-lookup"><span data-stu-id="76ddf-112">Number of request body bytes to log.</span></span> <span data-ttu-id="76ddf-113">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="76ddf-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="76ddf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76ddf-114">-DefaultProfile</span></span>
<span data-ttu-id="76ddf-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="76ddf-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76ddf-116">-HeadersToLog</span><span class="sxs-lookup"><span data-stu-id="76ddf-116">-HeadersToLog</span></span>
<span data-ttu-id="76ddf-117">Tablica nagłówków do dziennika.</span><span class="sxs-lookup"><span data-stu-id="76ddf-117">The array of headers to log.</span></span> <span data-ttu-id="76ddf-118">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="76ddf-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="76ddf-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76ddf-119">CommonParameters</span></span>
<span data-ttu-id="76ddf-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76ddf-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76ddf-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="76ddf-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76ddf-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="76ddf-122">INPUTS</span></span>

### <span data-ttu-id="76ddf-123">Brak</span><span class="sxs-lookup"><span data-stu-id="76ddf-123">None</span></span>

## <span data-ttu-id="76ddf-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="76ddf-124">OUTPUTS</span></span>

### <span data-ttu-id="76ddf-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.psApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="76ddf-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic</span></span>

## <span data-ttu-id="76ddf-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="76ddf-126">NOTES</span></span>

## <span data-ttu-id="76ddf-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="76ddf-127">RELATED LINKS</span></span>

[<span data-ttu-id="76ddf-128">New-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="76ddf-128">New-AzApiManagementDiagnostic</span></span>](./New-AzApiManagementDiagnostic.md)

[<span data-ttu-id="76ddf-129">New-AzApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="76ddf-129">New-AzApiManagementSamplingSetting</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)