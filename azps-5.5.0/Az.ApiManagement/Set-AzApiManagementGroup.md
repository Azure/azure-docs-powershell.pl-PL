---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 66D543C0-34F0-47B1-943A-415DECF2155C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementGroup.md
ms.openlocfilehash: f4e2bb2bce0dc01f99b55497ba671999c9c2ab01
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199707"
---
# <span data-ttu-id="e1b56-101">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="e1b56-101">Set-AzApiManagementGroup</span></span>

## <span data-ttu-id="e1b56-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1b56-102">SYNOPSIS</span></span>
<span data-ttu-id="e1b56-103">Konfiguruje grupę zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="e1b56-103">Configures an API management group.</span></span>

## <span data-ttu-id="e1b56-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e1b56-104">SYNTAX</span></span>

```
Set-AzApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-Name <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e1b56-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="e1b56-105">DESCRIPTION</span></span>
<span data-ttu-id="e1b56-106">Polecenie **cmdlet Set-AzApiManagementGroup** konfiguruje grupę zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="e1b56-106">The **Set-AzApiManagementGroup** cmdlet configures an API management group.</span></span>

## <span data-ttu-id="e1b56-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e1b56-107">EXAMPLES</span></span>

### <span data-ttu-id="e1b56-108">Przykład 1. Konfigurowanie grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="e1b56-108">Example 1: Configure a management group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementGroup -Context $apimContext -GroupId "0001" -Description "Updated Management Group" -Name "Group0001"
```

<span data-ttu-id="e1b56-109">To polecenie konfiguruje grupę zarządzania o nazwie Group0001.</span><span class="sxs-lookup"><span data-stu-id="e1b56-109">This command configures a management group named Group0001.</span></span>

## <span data-ttu-id="e1b56-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e1b56-110">PARAMETERS</span></span>

### <span data-ttu-id="e1b56-111">— kontekst</span><span class="sxs-lookup"><span data-stu-id="e1b56-111">-Context</span></span>
<span data-ttu-id="e1b56-112">Określa wystąpienie obiektu **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="e1b56-112">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="e1b56-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1b56-113">-DefaultProfile</span></span>
<span data-ttu-id="e1b56-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e1b56-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1b56-115">— Opis</span><span class="sxs-lookup"><span data-stu-id="e1b56-115">-Description</span></span>
<span data-ttu-id="e1b56-116">Określa opis grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="e1b56-116">Specifies the description of the management group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1b56-117">- GroupId</span><span class="sxs-lookup"><span data-stu-id="e1b56-117">-GroupId</span></span>
<span data-ttu-id="e1b56-118">Określa identyfikator grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="e1b56-118">Specifies the identifier of the management group.</span></span>

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

### <span data-ttu-id="e1b56-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e1b56-119">-Name</span></span>
<span data-ttu-id="e1b56-120">Określa nazwę grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="e1b56-120">Specifies the name of the management group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1b56-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e1b56-121">-PassThru</span></span>
<span data-ttu-id="e1b56-122">passthru</span><span class="sxs-lookup"><span data-stu-id="e1b56-122">passthru</span></span>

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

### <span data-ttu-id="e1b56-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e1b56-123">-Confirm</span></span>
<span data-ttu-id="e1b56-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e1b56-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1b56-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1b56-125">-WhatIf</span></span>
<span data-ttu-id="e1b56-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1b56-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e1b56-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e1b56-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1b56-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1b56-128">CommonParameters</span></span>
<span data-ttu-id="e1b56-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1b56-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1b56-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e1b56-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1b56-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e1b56-131">INPUTS</span></span>

### <span data-ttu-id="e1b56-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e1b56-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e1b56-133">System.String</span><span class="sxs-lookup"><span data-stu-id="e1b56-133">System.String</span></span>

### <span data-ttu-id="e1b56-134">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="e1b56-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e1b56-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e1b56-135">OUTPUTS</span></span>

### <span data-ttu-id="e1b56-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="e1b56-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="e1b56-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e1b56-137">NOTES</span></span>

## <span data-ttu-id="e1b56-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e1b56-138">RELATED LINKS</span></span>

[<span data-ttu-id="e1b56-139">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="e1b56-139">Get-AzApiManagementGroup</span></span>](./Get-AzApiManagementGroup.md)

[<span data-ttu-id="e1b56-140">New-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="e1b56-140">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="e1b56-141">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="e1b56-141">Remove-AzApiManagementGroup</span></span>](./Remove-AzApiManagementGroup.md)


