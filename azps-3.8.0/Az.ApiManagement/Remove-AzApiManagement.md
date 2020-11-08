---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: CD582654-1B0C-4960-9E18-454F857B56E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagement.md
ms.openlocfilehash: f54998dc0d5ec8570a573870148a8cf05c265618
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051172"
---
# <span data-ttu-id="00c6c-101">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="00c6c-101">Remove-AzApiManagement</span></span>

## <span data-ttu-id="00c6c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="00c6c-102">SYNOPSIS</span></span>
<span data-ttu-id="00c6c-103">Usuwa usługę zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="00c6c-103">Removes an API Management service.</span></span>

## <span data-ttu-id="00c6c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="00c6c-104">SYNTAX</span></span>

```
Remove-AzApiManagement -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00c6c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="00c6c-105">DESCRIPTION</span></span>
<span data-ttu-id="00c6c-106">Polecenie cmdlet **Remove-AzApiManagement** usuwa usługę zarządzania interfejsem Azure API.</span><span class="sxs-lookup"><span data-stu-id="00c6c-106">The **Remove-AzApiManagement** cmdlet removes an Azure API Management service.</span></span>

## <span data-ttu-id="00c6c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="00c6c-107">EXAMPLES</span></span>

### <span data-ttu-id="00c6c-108">Przykład 1: Usuwanie usługi zarządzania interfejsem API</span><span class="sxs-lookup"><span data-stu-id="00c6c-108">Example 1: Remove an API Management service</span></span>
```
PS C:\>Remove-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi"
```

<span data-ttu-id="00c6c-109">To polecenie usuwa usługę zarządzania interfejsem API o nazwie ContosoApi.</span><span class="sxs-lookup"><span data-stu-id="00c6c-109">This command removes the API Management service named ContosoApi.</span></span>

## <span data-ttu-id="00c6c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="00c6c-110">PARAMETERS</span></span>

### <span data-ttu-id="00c6c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00c6c-111">-DefaultProfile</span></span>
<span data-ttu-id="00c6c-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="00c6c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00c6c-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="00c6c-113">-Name</span></span>
<span data-ttu-id="00c6c-114">Określa nazwę wdrożenia zarządzania interfejsem API, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00c6c-114">Specifies the name of the API Management deployment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="00c6c-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="00c6c-115">-PassThru</span></span>
<span data-ttu-id="00c6c-116">Wskazuje, że to polecenie cmdlet zwraca wartość $True, jeśli operacja się powiedzie.</span><span class="sxs-lookup"><span data-stu-id="00c6c-116">Indicates that this cmdlet returns a value of $True if the operation succeeds.</span></span>

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

### <span data-ttu-id="00c6c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00c6c-117">-ResourceGroupName</span></span>
<span data-ttu-id="00c6c-118">Określa nazwę grupy zasobów, w której istnieje wdrożenie zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="00c6c-118">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

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

### <span data-ttu-id="00c6c-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="00c6c-119">-Confirm</span></span>
<span data-ttu-id="00c6c-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00c6c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00c6c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00c6c-121">-WhatIf</span></span>
<span data-ttu-id="00c6c-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00c6c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00c6c-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="00c6c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00c6c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00c6c-124">CommonParameters</span></span>
<span data-ttu-id="00c6c-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00c6c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00c6c-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="00c6c-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00c6c-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="00c6c-127">INPUTS</span></span>

### <span data-ttu-id="00c6c-128">System. String</span><span class="sxs-lookup"><span data-stu-id="00c6c-128">System.String</span></span>

## <span data-ttu-id="00c6c-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="00c6c-129">OUTPUTS</span></span>

### <span data-ttu-id="00c6c-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="00c6c-130">System.Boolean</span></span>

## <span data-ttu-id="00c6c-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="00c6c-131">NOTES</span></span>

## <span data-ttu-id="00c6c-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="00c6c-132">RELATED LINKS</span></span>

[<span data-ttu-id="00c6c-133">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="00c6c-133">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="00c6c-134">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="00c6c-134">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="00c6c-135">Nowe — AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="00c6c-135">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="00c6c-136">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="00c6c-136">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


