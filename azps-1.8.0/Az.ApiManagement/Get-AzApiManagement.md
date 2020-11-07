---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: DBA7AD5F-CC13-417A-B753-F998942530BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagement.md
ms.openlocfilehash: c636da952c02b4f2b4795cd1703c276a23a8221c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93704668"
---
# <span data-ttu-id="b1c12-101">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="b1c12-101">Get-AzApiManagement</span></span>

## <span data-ttu-id="b1c12-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b1c12-102">SYNOPSIS</span></span>
<span data-ttu-id="b1c12-103">Pobiera listę lub określony Opis usługi zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="b1c12-103">Gets a list or a particular API Management Service description.</span></span>

## <span data-ttu-id="b1c12-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b1c12-104">SYNTAX</span></span>

### <span data-ttu-id="b1c12-105">GetBySubscription (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b1c12-105">GetBySubscription (Default)</span></span>
```
Get-AzApiManagement [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1c12-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b1c12-106">GetByResourceGroup</span></span>
```
Get-AzApiManagement -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1c12-107">GetByResource</span><span class="sxs-lookup"><span data-stu-id="b1c12-107">GetByResource</span></span>
```
Get-AzApiManagement -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b1c12-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b1c12-108">DESCRIPTION</span></span>
<span data-ttu-id="b1c12-109">Polecenie cmdlet **Get-AzApiManagement** pobiera listę wszystkich usług zarządzania API w obszarze subskrypcja lub określona grupa zasobów lub w ramach określonego zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="b1c12-109">The **Get-AzApiManagement** cmdlet gets a list of all API Management services under subscription or specified resource group or a particular API Management.</span></span>

## <span data-ttu-id="b1c12-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b1c12-110">EXAMPLES</span></span>

### <span data-ttu-id="b1c12-111">Przykład 1: uzyskiwanie wszystkich usług zarządzania interfejsem API</span><span class="sxs-lookup"><span data-stu-id="b1c12-111">Example 1: Get all API Management services</span></span>
```powershell
PS C:\>Get-AzApiManagement
```

<span data-ttu-id="b1c12-112">To polecenie pobiera wszystkie usługi zarządzania API w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="b1c12-112">This command gets all API Management services within a subscription.</span></span>

### <span data-ttu-id="b1c12-113">Przykład 2: uzyskiwanie wszystkich usług zarządzania interfejsem API według określonej nazwy</span><span class="sxs-lookup"><span data-stu-id="b1c12-113">Example 2: Get all API Management services by a specific name</span></span>
```powershell
PS C:\>Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
```

<span data-ttu-id="b1c12-114">To polecenie pobiera całą usługę zarządzania interfejsem API według nazwy.</span><span class="sxs-lookup"><span data-stu-id="b1c12-114">This command gets all API Management service by name.</span></span>

## <span data-ttu-id="b1c12-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b1c12-115">PARAMETERS</span></span>

### <span data-ttu-id="b1c12-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1c12-116">-DefaultProfile</span></span>
<span data-ttu-id="b1c12-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b1c12-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1c12-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b1c12-118">-Name</span></span>
<span data-ttu-id="b1c12-119">Określa nazwę usługi zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="b1c12-119">Specifies the name of API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1c12-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1c12-120">-ResourceGroupName</span></span>
<span data-ttu-id="b1c12-121">Określa nazwę grupy zasobów, w której ten aplet polecenia pobiera usługę zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="b1c12-121">Specifies the name of the resource group under in which this cmdlet gets the API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup, GetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1c12-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1c12-122">CommonParameters</span></span>
<span data-ttu-id="b1c12-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1c12-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1c12-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1c12-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1c12-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b1c12-125">INPUTS</span></span>

### <span data-ttu-id="b1c12-126">System. String</span><span class="sxs-lookup"><span data-stu-id="b1c12-126">System.String</span></span>

## <span data-ttu-id="b1c12-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b1c12-127">OUTPUTS</span></span>

### <span data-ttu-id="b1c12-128">Microsoft. Azure. Commands. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="b1c12-128">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="b1c12-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b1c12-129">NOTES</span></span>

## <span data-ttu-id="b1c12-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b1c12-130">RELATED LINKS</span></span>

[<span data-ttu-id="b1c12-131">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="b1c12-131">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="b1c12-132">Nowe — AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="b1c12-132">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="b1c12-133">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="b1c12-133">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="b1c12-134">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="b1c12-134">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


