---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: CD582654-1B0C-4960-9E18-454F857B56E7
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagement.md
ms.openlocfilehash: daa4169ed077003d2ceb773e2e085e72fb6d1ec8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959153"
---
# <span data-ttu-id="77e37-101">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="77e37-101">Remove-AzApiManagement</span></span>

## <span data-ttu-id="77e37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77e37-102">SYNOPSIS</span></span>
<span data-ttu-id="77e37-103">Usuwa usługę zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="77e37-103">Removes an API Management service.</span></span>

## <span data-ttu-id="77e37-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="77e37-104">SYNTAX</span></span>

```
Remove-AzApiManagement -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77e37-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="77e37-105">DESCRIPTION</span></span>
<span data-ttu-id="77e37-106">Polecenie **cmdlet Remove-AzApiManagement** usuwa usługę Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="77e37-106">The **Remove-AzApiManagement** cmdlet removes an Azure API Management service.</span></span>

## <span data-ttu-id="77e37-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="77e37-107">EXAMPLES</span></span>

### <span data-ttu-id="77e37-108">Przykład 1. Usuwanie usługi zarządzania interfejsem API</span><span class="sxs-lookup"><span data-stu-id="77e37-108">Example 1: Remove an API Management service</span></span>
```
PS C:\>Remove-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi"
```

<span data-ttu-id="77e37-109">To polecenie usuwa usługę zarządzania interfejsem API o nazwie ContosoApi.</span><span class="sxs-lookup"><span data-stu-id="77e37-109">This command removes the API Management service named ContosoApi.</span></span>

## <span data-ttu-id="77e37-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="77e37-110">PARAMETERS</span></span>

### <span data-ttu-id="77e37-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77e37-111">-DefaultProfile</span></span>
<span data-ttu-id="77e37-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="77e37-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="77e37-113">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="77e37-113">-Name</span></span>
<span data-ttu-id="77e37-114">Określa nazwę wdrożenia zarządzania interfejsem API, które usuwa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77e37-114">Specifies the name of the API Management deployment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="77e37-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="77e37-115">-PassThru</span></span>
<span data-ttu-id="77e37-116">Wskazuje, że to polecenie cmdlet zwraca wartość $True, jeśli operacja się powiedzie.</span><span class="sxs-lookup"><span data-stu-id="77e37-116">Indicates that this cmdlet returns a value of $True if the operation succeeds.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77e37-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77e37-117">-ResourceGroupName</span></span>
<span data-ttu-id="77e37-118">Określa nazwę grupy zasobów, w ramach której istnieje wdrożenie Zarządzanie interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="77e37-118">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

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

### <span data-ttu-id="77e37-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="77e37-119">-Confirm</span></span>
<span data-ttu-id="77e37-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="77e37-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77e37-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77e37-121">-WhatIf</span></span>
<span data-ttu-id="77e37-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77e37-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77e37-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="77e37-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77e37-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77e37-124">CommonParameters</span></span>
<span data-ttu-id="77e37-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77e37-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77e37-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="77e37-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77e37-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="77e37-127">INPUTS</span></span>

### <span data-ttu-id="77e37-128">System.String</span><span class="sxs-lookup"><span data-stu-id="77e37-128">System.String</span></span>

## <span data-ttu-id="77e37-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="77e37-129">OUTPUTS</span></span>

### <span data-ttu-id="77e37-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="77e37-130">System.Boolean</span></span>

## <span data-ttu-id="77e37-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="77e37-131">NOTES</span></span>

## <span data-ttu-id="77e37-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="77e37-132">RELATED LINKS</span></span>

[<span data-ttu-id="77e37-133">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="77e37-133">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="77e37-134">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="77e37-134">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="77e37-135">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="77e37-135">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="77e37-136">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="77e37-136">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


