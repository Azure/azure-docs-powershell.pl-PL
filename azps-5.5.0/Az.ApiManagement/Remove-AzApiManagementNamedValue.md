---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementnamedvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementNamedValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementNamedValue.md
ms.openlocfilehash: c2cf7f46a7f7f73443a9d7d2b06dbfde943b28d0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199730"
---
# <span data-ttu-id="24050-101">Remove-AzApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="24050-101">Remove-AzApiManagementNamedValue</span></span>

## <span data-ttu-id="24050-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24050-102">SYNOPSIS</span></span>
<span data-ttu-id="24050-103">Usuwa wartość nazwaną zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="24050-103">Removes an API Management Named Value.</span></span>

## <span data-ttu-id="24050-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="24050-104">SYNTAX</span></span>

```
Remove-AzApiManagementNamedValue -Context <PsApiManagementContext> -NamedValueId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24050-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="24050-105">DESCRIPTION</span></span>
<span data-ttu-id="24050-106">Polecenie **cmdlet Remove-AzApiManagementNamedValue** usuwa wartość nazwaną usługi Azure API **Management.**</span><span class="sxs-lookup"><span data-stu-id="24050-106">The **Remove-AzApiManagementNamedValue** cmdlet removes an Azure API Management **Named Value**.</span></span>

## <span data-ttu-id="24050-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="24050-107">EXAMPLES</span></span>

### <span data-ttu-id="24050-108">Przykład 1. Usuwanie nazwanej wartości</span><span class="sxs-lookup"><span data-stu-id="24050-108">Example 1: Remove the named value</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementNamedValue -Context $apimContext -NamedValueId "Property11" -PassThru
```

<span data-ttu-id="24050-109">To polecenie usuwa nazwaną wartość, która ma właściwość ID11.</span><span class="sxs-lookup"><span data-stu-id="24050-109">This command removes the named value that has the ID Property11.</span></span>

## <span data-ttu-id="24050-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="24050-110">PARAMETERS</span></span>

### <span data-ttu-id="24050-111">— kontekst</span><span class="sxs-lookup"><span data-stu-id="24050-111">-Context</span></span>
<span data-ttu-id="24050-112">Wystąpienie tekstu PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="24050-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="24050-113">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="24050-113">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="24050-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24050-114">-DefaultProfile</span></span>
<span data-ttu-id="24050-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="24050-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24050-116">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="24050-116">-NamedValueId</span></span>
<span data-ttu-id="24050-117">Identyfikator istniejącej nazwanej wartości.</span><span class="sxs-lookup"><span data-stu-id="24050-117">Identifier of existing named value.</span></span>
<span data-ttu-id="24050-118">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="24050-118">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24050-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="24050-119">-PassThru</span></span>
<span data-ttu-id="24050-120">Jeśli zostanie określona, na wypadek, gdyby operacja zakończyła się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="24050-120">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="24050-121">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="24050-121">This parameter is optional.</span></span>
<span data-ttu-id="24050-122">Wartość domyślna to fałsz.</span><span class="sxs-lookup"><span data-stu-id="24050-122">Default value is false.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24050-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="24050-123">-Confirm</span></span>
<span data-ttu-id="24050-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="24050-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24050-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24050-125">-WhatIf</span></span>
<span data-ttu-id="24050-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24050-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24050-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="24050-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24050-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24050-128">CommonParameters</span></span>
<span data-ttu-id="24050-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24050-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24050-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="24050-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24050-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="24050-131">INPUTS</span></span>

### <span data-ttu-id="24050-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="24050-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="24050-133">System.String</span><span class="sxs-lookup"><span data-stu-id="24050-133">System.String</span></span>

### <span data-ttu-id="24050-134">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="24050-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="24050-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="24050-135">OUTPUTS</span></span>

### <span data-ttu-id="24050-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="24050-136">System.Boolean</span></span>

## <span data-ttu-id="24050-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="24050-137">NOTES</span></span>

## <span data-ttu-id="24050-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="24050-138">RELATED LINKS</span></span>
