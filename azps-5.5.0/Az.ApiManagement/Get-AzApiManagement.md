---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: DBA7AD5F-CC13-417A-B753-F998942530BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagement.md
ms.openlocfilehash: 41f7b921cb1977d7410c511be224b7e24623597b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192562"
---
# <span data-ttu-id="17f67-101">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="17f67-101">Get-AzApiManagement</span></span>

## <span data-ttu-id="17f67-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17f67-102">SYNOPSIS</span></span>
<span data-ttu-id="17f67-103">Pobiera listę lub określony opis usługi zarządzania interfejsami API.</span><span class="sxs-lookup"><span data-stu-id="17f67-103">Gets a list or a particular API Management Service description.</span></span>

## <span data-ttu-id="17f67-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="17f67-104">SYNTAX</span></span>

### <span data-ttu-id="17f67-105">GetBySubscription (domyślne)</span><span class="sxs-lookup"><span data-stu-id="17f67-105">GetBySubscription (Default)</span></span>
```
Get-AzApiManagement [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17f67-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="17f67-106">GetByResourceGroup</span></span>
```
Get-AzApiManagement -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17f67-107">GetByResource</span><span class="sxs-lookup"><span data-stu-id="17f67-107">GetByResource</span></span>
```
Get-AzApiManagement -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="17f67-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="17f67-108">ByResourceId</span></span>
```
Get-AzApiManagement -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17f67-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="17f67-109">DESCRIPTION</span></span>
<span data-ttu-id="17f67-110">Polecenie **cmdlet Get-AzApiManagement** pobiera listę wszystkich usług zarządzania interfejsem API w ramach subskrypcji, określonej grupy zasobów lub konkretnego zarządzania interfejsami API.</span><span class="sxs-lookup"><span data-stu-id="17f67-110">The **Get-AzApiManagement** cmdlet gets a list of all API Management services under subscription or specified resource group or a particular API Management.</span></span>

## <span data-ttu-id="17f67-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="17f67-111">EXAMPLES</span></span>

### <span data-ttu-id="17f67-112">Przykład 1. Uzyskiwanie wszystkich usług zarządzania interfejsami API</span><span class="sxs-lookup"><span data-stu-id="17f67-112">Example 1: Get all API Management services</span></span>
```powershell
PS C:\>Get-AzApiManagement
```

<span data-ttu-id="17f67-113">To polecenie pobiera wszystkie usługi zarządzania interfejsami API w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="17f67-113">This command gets all API Management services within a subscription.</span></span>

### <span data-ttu-id="17f67-114">Przykład 2. Uzyskiwanie wszystkich usług zarządzania interfejsem API według określonej nazwy</span><span class="sxs-lookup"><span data-stu-id="17f67-114">Example 2: Get all API Management services by a specific name</span></span>
```powershell
PS C:\>Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
```

<span data-ttu-id="17f67-115">To polecenie otrzymuje według nazwy wszystkie usługi zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="17f67-115">This command gets all API Management service by name.</span></span>

## <span data-ttu-id="17f67-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="17f67-116">PARAMETERS</span></span>

### <span data-ttu-id="17f67-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17f67-117">-DefaultProfile</span></span>
<span data-ttu-id="17f67-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="17f67-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="17f67-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="17f67-119">-Name</span></span>
<span data-ttu-id="17f67-120">Określa nazwę usługi zarządzania interfejsami API.</span><span class="sxs-lookup"><span data-stu-id="17f67-120">Specifies the name of API Management service.</span></span>

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

### <span data-ttu-id="17f67-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17f67-121">-ResourceGroupName</span></span>
<span data-ttu-id="17f67-122">Określa nazwę grupy zasobów, w której to polecenie cmdlet pobiera usługę zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="17f67-122">Specifies the name of the resource group under in which this cmdlet gets the API Management service.</span></span>

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

### <span data-ttu-id="17f67-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="17f67-123">-ResourceId</span></span>
<span data-ttu-id="17f67-124">Arm ResourceId usługi zarządzania interfejsami API.</span><span class="sxs-lookup"><span data-stu-id="17f67-124">Arm ResourceId of the API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17f67-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17f67-125">CommonParameters</span></span>
<span data-ttu-id="17f67-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17f67-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17f67-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="17f67-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17f67-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="17f67-128">INPUTS</span></span>

### <span data-ttu-id="17f67-129">System.String</span><span class="sxs-lookup"><span data-stu-id="17f67-129">System.String</span></span>

## <span data-ttu-id="17f67-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="17f67-130">OUTPUTS</span></span>

### <span data-ttu-id="17f67-131">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="17f67-131">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="17f67-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="17f67-132">NOTES</span></span>

## <span data-ttu-id="17f67-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="17f67-133">RELATED LINKS</span></span>

[<span data-ttu-id="17f67-134">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="17f67-134">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="17f67-135">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="17f67-135">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="17f67-136">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="17f67-136">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="17f67-137">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="17f67-137">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


