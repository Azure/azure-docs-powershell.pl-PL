---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: F23D9274-63B9-4654-897B-6E84757774D2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApi.md
ms.openlocfilehash: cadae96af05ae11f76d3a8ea0010da4d73161186
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525790"
---
# <span data-ttu-id="67588-101">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="67588-101">Remove-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="67588-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="67588-102">SYNOPSIS</span></span>
<span data-ttu-id="67588-103">Usuwa interfejs API.</span><span class="sxs-lookup"><span data-stu-id="67588-103">Removes an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67588-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="67588-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67588-105">Opis</span><span class="sxs-lookup"><span data-stu-id="67588-105">DESCRIPTION</span></span>
<span data-ttu-id="67588-106">Polecenie cmdlet **Remove-AzureRmApiManagementApi** usuwa istniejący interfejs API.</span><span class="sxs-lookup"><span data-stu-id="67588-106">The **Remove-AzureRmApiManagementApi** cmdlet removes an existing API.</span></span>

## <span data-ttu-id="67588-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="67588-107">EXAMPLES</span></span>

### <span data-ttu-id="67588-108">Przykład 1: Usuwanie interfejsu API</span><span class="sxs-lookup"><span data-stu-id="67588-108">Example 1: Remove an API</span></span>
```
PS C:\>Remove-AzureRmApiManagementApi -Context $ApiMgmtContext -ApiId "0123456789"
```

<span data-ttu-id="67588-109">To polecenie usuwa interfejs API o określonym IDENTYFIKATORze.</span><span class="sxs-lookup"><span data-stu-id="67588-109">This command removes the API with the specified ID.</span></span>

## <span data-ttu-id="67588-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="67588-110">PARAMETERS</span></span>

### <span data-ttu-id="67588-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="67588-111">-ApiId</span></span>
<span data-ttu-id="67588-112">Określa identyfikator interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="67588-112">Specifies the ID of the API remove.</span></span>

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

### <span data-ttu-id="67588-113">-Context</span><span class="sxs-lookup"><span data-stu-id="67588-113">-Context</span></span>
<span data-ttu-id="67588-114">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="67588-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="67588-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="67588-115">-PassThru</span></span>
<span data-ttu-id="67588-116">passthru</span><span class="sxs-lookup"><span data-stu-id="67588-116">passthru</span></span>

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

### <span data-ttu-id="67588-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="67588-117">-Confirm</span></span>
<span data-ttu-id="67588-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67588-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67588-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67588-119">-WhatIf</span></span>
<span data-ttu-id="67588-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67588-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67588-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="67588-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67588-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67588-122">-DefaultProfile</span></span>
<span data-ttu-id="67588-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="67588-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67588-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67588-124">CommonParameters</span></span>
<span data-ttu-id="67588-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67588-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67588-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67588-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67588-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="67588-127">INPUTS</span></span>

## <span data-ttu-id="67588-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="67588-128">OUTPUTS</span></span>

### <span data-ttu-id="67588-129">Wartość</span><span class="sxs-lookup"><span data-stu-id="67588-129">Boolean</span></span>

## <span data-ttu-id="67588-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="67588-130">NOTES</span></span>

## <span data-ttu-id="67588-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="67588-131">RELATED LINKS</span></span>

[<span data-ttu-id="67588-132">Eksportowanie — AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="67588-132">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="67588-133">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="67588-133">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="67588-134">Import — AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="67588-134">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="67588-135">Nowe — AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="67588-135">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="67588-136">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="67588-136">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


