---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: D3C60123-CE1F-45F1-8C8F-25CDC302490C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProperty.md
ms.openlocfilehash: ea063de747f69d10660fe8117d34647156694b5b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869403"
---
# <span data-ttu-id="1a754-101">Remove-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="1a754-101">Remove-AzApiManagementProperty</span></span>

## <span data-ttu-id="1a754-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1a754-102">SYNOPSIS</span></span>
<span data-ttu-id="1a754-103">Usuwa Właściwość zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="1a754-103">Removes an API Management Property.</span></span>

## <span data-ttu-id="1a754-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1a754-104">SYNTAX</span></span>

```
Remove-AzApiManagementProperty -Context <PsApiManagementContext> -PropertyId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a754-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1a754-105">DESCRIPTION</span></span>
<span data-ttu-id="1a754-106">Polecenie cmdlet **Remove-AzApiManagementProperty** usuwa **Właściwość** zarządzanie interfejsem Azure API.</span><span class="sxs-lookup"><span data-stu-id="1a754-106">The **Remove-AzApiManagementProperty** cmdlet removes an Azure API Management **Property**.</span></span>

## <span data-ttu-id="1a754-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1a754-107">EXAMPLES</span></span>

### <span data-ttu-id="1a754-108">Przykład 1. Usuń właściwość</span><span class="sxs-lookup"><span data-stu-id="1a754-108">Example 1: Remove a property</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementProperty -Context $apimContext -PropertyId "Property11" -PassThru
```

<span data-ttu-id="1a754-109">To polecenie usuwa właściwość o IDENTYFIKATORze Property11.</span><span class="sxs-lookup"><span data-stu-id="1a754-109">This command removes the property that has the ID Property11.</span></span>

## <span data-ttu-id="1a754-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1a754-110">PARAMETERS</span></span>

### <span data-ttu-id="1a754-111">-Context</span><span class="sxs-lookup"><span data-stu-id="1a754-111">-Context</span></span>
<span data-ttu-id="1a754-112">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="1a754-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="1a754-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a754-113">-DefaultProfile</span></span>
<span data-ttu-id="1a754-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1a754-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1a754-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1a754-115">-PassThru</span></span>
<span data-ttu-id="1a754-116">Wskazuje, że to polecenie cmdlet zwraca wartość $True, jeśli operacja się powiedzie lub $False w inny sposób.</span><span class="sxs-lookup"><span data-stu-id="1a754-116">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="1a754-117">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="1a754-117">-PropertyId</span></span>
<span data-ttu-id="1a754-118">Określa identyfikator właściwości, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a754-118">Specifies an ID of the property that this cmdlet removes.</span></span>

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

### <span data-ttu-id="1a754-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1a754-119">-Confirm</span></span>
<span data-ttu-id="1a754-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a754-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a754-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a754-121">-WhatIf</span></span>
<span data-ttu-id="1a754-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a754-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a754-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1a754-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a754-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a754-124">CommonParameters</span></span>
<span data-ttu-id="1a754-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a754-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a754-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a754-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a754-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1a754-127">INPUTS</span></span>

### <span data-ttu-id="1a754-128">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="1a754-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1a754-129">System. String</span><span class="sxs-lookup"><span data-stu-id="1a754-129">System.String</span></span>

### <span data-ttu-id="1a754-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1a754-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1a754-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1a754-131">OUTPUTS</span></span>

### <span data-ttu-id="1a754-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1a754-132">System.Boolean</span></span>

## <span data-ttu-id="1a754-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1a754-133">NOTES</span></span>

## <span data-ttu-id="1a754-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1a754-134">RELATED LINKS</span></span>

[<span data-ttu-id="1a754-135">Nowe — AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="1a754-135">New-AzApiManagementProperty</span></span>](./New-AzApiManagementProperty.md)

[<span data-ttu-id="1a754-136">Set-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="1a754-136">Set-AzApiManagementProperty</span></span>](./Set-AzApiManagementProperty.md)


