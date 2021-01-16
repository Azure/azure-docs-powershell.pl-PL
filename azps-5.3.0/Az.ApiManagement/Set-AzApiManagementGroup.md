---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 66D543C0-34F0-47B1-943A-415DECF2155C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementGroup.md
ms.openlocfilehash: f4e2bb2bce0dc01f99b55497ba671999c9c2ab01
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98381745"
---
# <span data-ttu-id="41cfd-101">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="41cfd-101">Set-AzApiManagementGroup</span></span>

## <span data-ttu-id="41cfd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="41cfd-102">SYNOPSIS</span></span>
<span data-ttu-id="41cfd-103">Umożliwia skonfigurowanie grupy zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="41cfd-103">Configures an API management group.</span></span>

## <span data-ttu-id="41cfd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="41cfd-104">SYNTAX</span></span>

```
Set-AzApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-Name <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="41cfd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="41cfd-105">DESCRIPTION</span></span>
<span data-ttu-id="41cfd-106">Polecenie cmdlet **Set-AzApiManagementGroup** umożliwia skonfigurowanie grupy zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="41cfd-106">The **Set-AzApiManagementGroup** cmdlet configures an API management group.</span></span>

## <span data-ttu-id="41cfd-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="41cfd-107">EXAMPLES</span></span>

### <span data-ttu-id="41cfd-108">Przykład 1: Konfigurowanie grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="41cfd-108">Example 1: Configure a management group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementGroup -Context $apimContext -GroupId "0001" -Description "Updated Management Group" -Name "Group0001"
```

<span data-ttu-id="41cfd-109">To polecenie umożliwia skonfigurowanie grupy zarządzania o nazwie Group0001.</span><span class="sxs-lookup"><span data-stu-id="41cfd-109">This command configures a management group named Group0001.</span></span>

## <span data-ttu-id="41cfd-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="41cfd-110">PARAMETERS</span></span>

### <span data-ttu-id="41cfd-111">-Context</span><span class="sxs-lookup"><span data-stu-id="41cfd-111">-Context</span></span>
<span data-ttu-id="41cfd-112">Określa wystąpienie obiektu **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="41cfd-112">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="41cfd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41cfd-113">-DefaultProfile</span></span>
<span data-ttu-id="41cfd-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="41cfd-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41cfd-115">— Opis</span><span class="sxs-lookup"><span data-stu-id="41cfd-115">-Description</span></span>
<span data-ttu-id="41cfd-116">Określa opis grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="41cfd-116">Specifies the description of the management group.</span></span>

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

### <span data-ttu-id="41cfd-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="41cfd-117">-GroupId</span></span>
<span data-ttu-id="41cfd-118">Określa identyfikator grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="41cfd-118">Specifies the identifier of the management group.</span></span>

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

### <span data-ttu-id="41cfd-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="41cfd-119">-Name</span></span>
<span data-ttu-id="41cfd-120">Określa nazwę grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="41cfd-120">Specifies the name of the management group.</span></span>

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

### <span data-ttu-id="41cfd-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="41cfd-121">-PassThru</span></span>
<span data-ttu-id="41cfd-122">passthru</span><span class="sxs-lookup"><span data-stu-id="41cfd-122">passthru</span></span>

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

### <span data-ttu-id="41cfd-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="41cfd-123">-Confirm</span></span>
<span data-ttu-id="41cfd-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41cfd-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41cfd-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41cfd-125">-WhatIf</span></span>
<span data-ttu-id="41cfd-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41cfd-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="41cfd-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="41cfd-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41cfd-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41cfd-128">CommonParameters</span></span>
<span data-ttu-id="41cfd-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41cfd-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41cfd-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="41cfd-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41cfd-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="41cfd-131">INPUTS</span></span>

### <span data-ttu-id="41cfd-132">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="41cfd-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="41cfd-133">System. String</span><span class="sxs-lookup"><span data-stu-id="41cfd-133">System.String</span></span>

### <span data-ttu-id="41cfd-134">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="41cfd-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="41cfd-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="41cfd-135">OUTPUTS</span></span>

### <span data-ttu-id="41cfd-136">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="41cfd-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="41cfd-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="41cfd-137">NOTES</span></span>

## <span data-ttu-id="41cfd-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="41cfd-138">RELATED LINKS</span></span>

[<span data-ttu-id="41cfd-139">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="41cfd-139">Get-AzApiManagementGroup</span></span>](./Get-AzApiManagementGroup.md)

[<span data-ttu-id="41cfd-140">Nowe — AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="41cfd-140">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="41cfd-141">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="41cfd-141">Remove-AzApiManagementGroup</span></span>](./Remove-AzApiManagementGroup.md)


