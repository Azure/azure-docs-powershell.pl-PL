---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementnamedvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementNamedValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementNamedValue.md
ms.openlocfilehash: c2cf7f46a7f7f73443a9d7d2b06dbfde943b28d0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063011"
---
# <span data-ttu-id="29fbf-101">Remove-AzApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="29fbf-101">Remove-AzApiManagementNamedValue</span></span>

## <span data-ttu-id="29fbf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="29fbf-102">SYNOPSIS</span></span>
<span data-ttu-id="29fbf-103">Usuwa wartość zarządzania interfejsem API o nazwie.</span><span class="sxs-lookup"><span data-stu-id="29fbf-103">Removes an API Management Named Value.</span></span>

## <span data-ttu-id="29fbf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="29fbf-104">SYNTAX</span></span>

```
Remove-AzApiManagementNamedValue -Context <PsApiManagementContext> -NamedValueId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29fbf-105">Opis</span><span class="sxs-lookup"><span data-stu-id="29fbf-105">DESCRIPTION</span></span>
<span data-ttu-id="29fbf-106">Polecenie cmdlet **Remove-AzApiManagementNamedValue** usuwa przystawkę Zarządzanie interfejsem Azure API **o nazwie Value**.</span><span class="sxs-lookup"><span data-stu-id="29fbf-106">The **Remove-AzApiManagementNamedValue** cmdlet removes an Azure API Management **Named Value**.</span></span>

## <span data-ttu-id="29fbf-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="29fbf-107">EXAMPLES</span></span>

### <span data-ttu-id="29fbf-108">Przykład 1. Usuń nazwaną wartość</span><span class="sxs-lookup"><span data-stu-id="29fbf-108">Example 1: Remove the named value</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementNamedValue -Context $apimContext -NamedValueId "Property11" -PassThru
```

<span data-ttu-id="29fbf-109">To polecenie usuwa nazwaną wartość o IDENTYFIKATORze Property11.</span><span class="sxs-lookup"><span data-stu-id="29fbf-109">This command removes the named value that has the ID Property11.</span></span>

## <span data-ttu-id="29fbf-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="29fbf-110">PARAMETERS</span></span>

### <span data-ttu-id="29fbf-111">-Context</span><span class="sxs-lookup"><span data-stu-id="29fbf-111">-Context</span></span>
<span data-ttu-id="29fbf-112">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="29fbf-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="29fbf-113">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="29fbf-113">This parameter is required.</span></span>

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

### <span data-ttu-id="29fbf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29fbf-114">-DefaultProfile</span></span>
<span data-ttu-id="29fbf-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="29fbf-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29fbf-116">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="29fbf-116">-NamedValueId</span></span>
<span data-ttu-id="29fbf-117">Identyfikator istniejącej wartości nazwanej.</span><span class="sxs-lookup"><span data-stu-id="29fbf-117">Identifier of existing named value.</span></span>
<span data-ttu-id="29fbf-118">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="29fbf-118">This parameter is required.</span></span>

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

### <span data-ttu-id="29fbf-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="29fbf-119">-PassThru</span></span>
<span data-ttu-id="29fbf-120">Jeśli ta wartość zostanie określona, operacja ta zostanie zapisana jako prawda w przypadku powodzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="29fbf-120">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="29fbf-121">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="29fbf-121">This parameter is optional.</span></span>
<span data-ttu-id="29fbf-122">Wartość domyślna to false.</span><span class="sxs-lookup"><span data-stu-id="29fbf-122">Default value is false.</span></span>

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

### <span data-ttu-id="29fbf-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="29fbf-123">-Confirm</span></span>
<span data-ttu-id="29fbf-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29fbf-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29fbf-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29fbf-125">-WhatIf</span></span>
<span data-ttu-id="29fbf-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29fbf-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29fbf-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="29fbf-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29fbf-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29fbf-128">CommonParameters</span></span>
<span data-ttu-id="29fbf-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29fbf-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29fbf-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="29fbf-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29fbf-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="29fbf-131">INPUTS</span></span>

### <span data-ttu-id="29fbf-132">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="29fbf-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="29fbf-133">System. String</span><span class="sxs-lookup"><span data-stu-id="29fbf-133">System.String</span></span>

### <span data-ttu-id="29fbf-134">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="29fbf-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="29fbf-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="29fbf-135">OUTPUTS</span></span>

### <span data-ttu-id="29fbf-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="29fbf-136">System.Boolean</span></span>

## <span data-ttu-id="29fbf-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="29fbf-137">NOTES</span></span>

## <span data-ttu-id="29fbf-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="29fbf-138">RELATED LINKS</span></span>
