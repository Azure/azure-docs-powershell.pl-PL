---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementresourcelocationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementResourceLocationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementResourceLocationObject.md
ms.openlocfilehash: 505264809b513ad144fa3812193fc39f86ab9b1e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98382417"
---
# <span data-ttu-id="82325-101">New-AzApiManagementResourceLocationObject</span><span class="sxs-lookup"><span data-stu-id="82325-101">New-AzApiManagementResourceLocationObject</span></span>

## <span data-ttu-id="82325-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="82325-102">SYNOPSIS</span></span>
<span data-ttu-id="82325-103">Tworzenie nowego kontraktu dotyczącego lokalizacji zasobów (używanej w bramach).</span><span class="sxs-lookup"><span data-stu-id="82325-103">Create a new resource location contract (used in Gateways).</span></span>

## <span data-ttu-id="82325-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="82325-104">SYNTAX</span></span>

```
New-AzApiManagementResourceLocationObject -Name <String> [-City <String>] [-District <String>]
 [-CountryOrRegion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82325-105">Opis</span><span class="sxs-lookup"><span data-stu-id="82325-105">DESCRIPTION</span></span>
<span data-ttu-id="82325-106">Polecenie cmdlet **New-AzApiManagementResourceLocationObject** Utwórz nowy kontrakt lokalizacji zasobów (używane w bramach).</span><span class="sxs-lookup"><span data-stu-id="82325-106">The **New-AzApiManagementResourceLocationObject** cmdlet create a new resource location contract (used in Gateways).</span></span>

## <span data-ttu-id="82325-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="82325-107">EXAMPLES</span></span>

### <span data-ttu-id="82325-108">Przykład 1. tworzenie kontraktu dotyczącego lokalizacji zasobów</span><span class="sxs-lookup"><span data-stu-id="82325-108">Example 1: Create a resource location contract</span></span>
```powershell
PS C:\>$location = New-AzApiManagementResourceLocationObject -Name "n1" -City "c1" -District "d1" -CountryOrRegion "r1"
```

<span data-ttu-id="82325-109">To polecenie tworzy lokalizację zasobów.</span><span class="sxs-lookup"><span data-stu-id="82325-109">This command creates a resource location.</span></span>

## <span data-ttu-id="82325-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="82325-110">PARAMETERS</span></span>

### <span data-ttu-id="82325-111">-Miasto</span><span class="sxs-lookup"><span data-stu-id="82325-111">-City</span></span>
<span data-ttu-id="82325-112">Miasto lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="82325-112">Location City.</span></span>
<span data-ttu-id="82325-113">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="82325-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="82325-114">-CountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="82325-114">-CountryOrRegion</span></span>
<span data-ttu-id="82325-115">Kraj lub region lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="82325-115">Location Country or Region.</span></span>
<span data-ttu-id="82325-116">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="82325-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="82325-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82325-117">-DefaultProfile</span></span>
<span data-ttu-id="82325-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="82325-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82325-119">-Dystrykt</span><span class="sxs-lookup"><span data-stu-id="82325-119">-District</span></span>
<span data-ttu-id="82325-120">Okręg lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="82325-120">Location District.</span></span>
<span data-ttu-id="82325-121">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="82325-121">This parameter is optional.</span></span>

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

### <span data-ttu-id="82325-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="82325-122">-Name</span></span>
<span data-ttu-id="82325-123">Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="82325-123">Location Name.</span></span>
<span data-ttu-id="82325-124">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="82325-124">This parameter is required.</span></span>

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

### <span data-ttu-id="82325-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82325-125">CommonParameters</span></span>
<span data-ttu-id="82325-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82325-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82325-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="82325-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82325-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="82325-128">INPUTS</span></span>

### <span data-ttu-id="82325-129">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="82325-129">None</span></span>

## <span data-ttu-id="82325-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="82325-130">OUTPUTS</span></span>

### <span data-ttu-id="82325-131">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementResourceLocation</span><span class="sxs-lookup"><span data-stu-id="82325-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span></span>

## <span data-ttu-id="82325-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="82325-132">NOTES</span></span>

## <span data-ttu-id="82325-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="82325-133">RELATED LINKS</span></span>
