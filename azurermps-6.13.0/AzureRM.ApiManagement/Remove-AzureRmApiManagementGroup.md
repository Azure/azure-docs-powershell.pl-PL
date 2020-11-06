---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: B88EC6DB-84AC-4F1D-AD79-0D243E0DC88A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementGroup.md
ms.openlocfilehash: d297c4f8bb9999d60ec694c73aa723dd4afec58f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524701"
---
# <span data-ttu-id="8d701-101">Remove-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="8d701-101">Remove-AzureRmApiManagementGroup</span></span>

## <span data-ttu-id="8d701-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8d701-102">SYNOPSIS</span></span>
<span data-ttu-id="8d701-103">Usuwa istniejącą grupę zarządzania interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="8d701-103">Removes an existing API management group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8d701-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8d701-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d701-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8d701-105">DESCRIPTION</span></span>
<span data-ttu-id="8d701-106">Polecenie cmdlet **Remove-AzureRmApiManagementGroup** Usuwa istniejącą grupę zarządzania interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="8d701-106">The **Remove-AzureRmApiManagementGroup** cmdlet removes an existing API management group.</span></span>

## <span data-ttu-id="8d701-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8d701-107">EXAMPLES</span></span>

### <span data-ttu-id="8d701-108">Przykład 1. Usuń istniejącą grupę zarządzania</span><span class="sxs-lookup"><span data-stu-id="8d701-108">Example 1: Remove an existing management group</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementGroup -Context $apimContext -GroupId "Group0001" -Force
```

<span data-ttu-id="8d701-109">To polecenie usuwa istniejącą grupę zarządzania o nazwie Group0001 i nie monituje użytkownika o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8d701-109">This command removes an existing management group named Group0001 and does not prompt the user for confirmation.</span></span>

## <span data-ttu-id="8d701-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8d701-110">PARAMETERS</span></span>

### <span data-ttu-id="8d701-111">-Context</span><span class="sxs-lookup"><span data-stu-id="8d701-111">-Context</span></span>
<span data-ttu-id="8d701-112">Określa wystąpienie obiektu **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="8d701-112">Specifies the instance of a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d701-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d701-113">-DefaultProfile</span></span>
<span data-ttu-id="8d701-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8d701-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d701-115">-GroupId</span><span class="sxs-lookup"><span data-stu-id="8d701-115">-GroupId</span></span>
<span data-ttu-id="8d701-116">Określa identyfikator grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="8d701-116">Specifies the identifier of a management group.</span></span>

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

### <span data-ttu-id="8d701-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8d701-117">-PassThru</span></span>
<span data-ttu-id="8d701-118">Wskazuje, że to polecenie cmdlet zwraca wartość $True, jeśli ta operacja się powiedzie lub wartość $False w przeciwnym razie.</span><span class="sxs-lookup"><span data-stu-id="8d701-118">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="8d701-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8d701-119">-Confirm</span></span>
<span data-ttu-id="8d701-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d701-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d701-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d701-121">-WhatIf</span></span>
<span data-ttu-id="8d701-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d701-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d701-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8d701-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d701-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d701-124">CommonParameters</span></span>
<span data-ttu-id="8d701-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d701-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d701-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d701-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d701-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8d701-127">INPUTS</span></span>

### <span data-ttu-id="8d701-128">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="8d701-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="8d701-129">System. String</span><span class="sxs-lookup"><span data-stu-id="8d701-129">System.String</span></span>

### <span data-ttu-id="8d701-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8d701-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8d701-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8d701-131">OUTPUTS</span></span>

### <span data-ttu-id="8d701-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8d701-132">System.Boolean</span></span>

## <span data-ttu-id="8d701-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8d701-133">NOTES</span></span>

## <span data-ttu-id="8d701-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8d701-134">RELATED LINKS</span></span>

[<span data-ttu-id="8d701-135">Get-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="8d701-135">Get-AzureRmApiManagementGroup</span></span>](./Get-AzureRmApiManagementGroup.md)

[<span data-ttu-id="8d701-136">Nowe — AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="8d701-136">New-AzureRmApiManagementGroup</span></span>](./New-AzureRmApiManagementGroup.md)

[<span data-ttu-id="8d701-137">Set-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="8d701-137">Set-AzureRmApiManagementGroup</span></span>](./Set-AzureRmApiManagementGroup.md)


