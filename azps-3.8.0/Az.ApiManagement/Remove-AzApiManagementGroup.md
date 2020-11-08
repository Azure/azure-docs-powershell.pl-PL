---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B88EC6DB-84AC-4F1D-AD79-0D243E0DC88A
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGroup.md
ms.openlocfilehash: 73e1fbee1dd20a9a30260727f693376346c87f0e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051121"
---
# <span data-ttu-id="edb4d-101">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="edb4d-101">Remove-AzApiManagementGroup</span></span>

## <span data-ttu-id="edb4d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="edb4d-102">SYNOPSIS</span></span>
<span data-ttu-id="edb4d-103">Usuwa istniejącą grupę zarządzania interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="edb4d-103">Removes an existing API management group.</span></span>

## <span data-ttu-id="edb4d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="edb4d-104">SYNTAX</span></span>

```
Remove-AzApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="edb4d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="edb4d-105">DESCRIPTION</span></span>
<span data-ttu-id="edb4d-106">Polecenie cmdlet **Remove-AzApiManagementGroup** Usuwa istniejącą grupę zarządzania interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="edb4d-106">The **Remove-AzApiManagementGroup** cmdlet removes an existing API management group.</span></span>

## <span data-ttu-id="edb4d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="edb4d-107">EXAMPLES</span></span>

### <span data-ttu-id="edb4d-108">Przykład 1. Usuń istniejącą grupę zarządzania</span><span class="sxs-lookup"><span data-stu-id="edb4d-108">Example 1: Remove an existing management group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementGroup -Context $apimContext -GroupId "Group0001" -Force
```

<span data-ttu-id="edb4d-109">To polecenie usuwa istniejącą grupę zarządzania o nazwie Group0001 i nie monituje użytkownika o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="edb4d-109">This command removes an existing management group named Group0001 and does not prompt the user for confirmation.</span></span>

## <span data-ttu-id="edb4d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="edb4d-110">PARAMETERS</span></span>

### <span data-ttu-id="edb4d-111">-Context</span><span class="sxs-lookup"><span data-stu-id="edb4d-111">-Context</span></span>
<span data-ttu-id="edb4d-112">Określa wystąpienie obiektu **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="edb4d-112">Specifies the instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="edb4d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edb4d-113">-DefaultProfile</span></span>
<span data-ttu-id="edb4d-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="edb4d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="edb4d-115">-GroupId</span><span class="sxs-lookup"><span data-stu-id="edb4d-115">-GroupId</span></span>
<span data-ttu-id="edb4d-116">Określa identyfikator grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="edb4d-116">Specifies the identifier of a management group.</span></span>

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

### <span data-ttu-id="edb4d-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="edb4d-117">-PassThru</span></span>
<span data-ttu-id="edb4d-118">Wskazuje, że to polecenie cmdlet zwraca wartość $True, jeśli ta operacja się powiedzie lub wartość $False w przeciwnym razie.</span><span class="sxs-lookup"><span data-stu-id="edb4d-118">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="edb4d-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="edb4d-119">-Confirm</span></span>
<span data-ttu-id="edb4d-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="edb4d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="edb4d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="edb4d-121">-WhatIf</span></span>
<span data-ttu-id="edb4d-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="edb4d-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="edb4d-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="edb4d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="edb4d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edb4d-124">CommonParameters</span></span>
<span data-ttu-id="edb4d-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="edb4d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edb4d-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="edb4d-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edb4d-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="edb4d-127">INPUTS</span></span>

### <span data-ttu-id="edb4d-128">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="edb4d-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="edb4d-129">System. String</span><span class="sxs-lookup"><span data-stu-id="edb4d-129">System.String</span></span>

### <span data-ttu-id="edb4d-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="edb4d-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="edb4d-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="edb4d-131">OUTPUTS</span></span>

### <span data-ttu-id="edb4d-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="edb4d-132">System.Boolean</span></span>

## <span data-ttu-id="edb4d-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="edb4d-133">NOTES</span></span>

## <span data-ttu-id="edb4d-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="edb4d-134">RELATED LINKS</span></span>

[<span data-ttu-id="edb4d-135">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="edb4d-135">Get-AzApiManagementGroup</span></span>](./Get-AzApiManagementGroup.md)

[<span data-ttu-id="edb4d-136">Nowe — AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="edb4d-136">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="edb4d-137">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="edb4d-137">Set-AzApiManagementGroup</span></span>](./Set-AzApiManagementGroup.md)


