---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: CD582654-1B0C-4960-9E18-454F857B56E7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagement.md
ms.openlocfilehash: 5a46e75f7ce7b0639de015de975c321c9d5c1ed6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525789"
---
# <span data-ttu-id="b13b0-101">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="b13b0-101">Remove-AzureRmApiManagement</span></span>

## <span data-ttu-id="b13b0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b13b0-102">SYNOPSIS</span></span>
<span data-ttu-id="b13b0-103">Usuwa usługę zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="b13b0-103">Removes an API Management service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b13b0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b13b0-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagement -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b13b0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b13b0-105">DESCRIPTION</span></span>
<span data-ttu-id="b13b0-106">Polecenie cmdlet **Remove-AzureRmApiManagement** usuwa usługę zarządzania interfejsem Azure API.</span><span class="sxs-lookup"><span data-stu-id="b13b0-106">The **Remove-AzureRmApiManagement** cmdlet removes an Azure API Management service.</span></span>

## <span data-ttu-id="b13b0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b13b0-107">EXAMPLES</span></span>

### <span data-ttu-id="b13b0-108">Przykład 1: Usuwanie usługi zarządzania interfejsem API</span><span class="sxs-lookup"><span data-stu-id="b13b0-108">Example 1: Remove an API Management service</span></span>
```
PS C:\>Remove-AzureRmApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi"
```

<span data-ttu-id="b13b0-109">To polecenie usuwa usługę zarządzania interfejsem API o nazwie ContosoApi.</span><span class="sxs-lookup"><span data-stu-id="b13b0-109">This command removes the API Management service named ContosoApi.</span></span>

## <span data-ttu-id="b13b0-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b13b0-110">PARAMETERS</span></span>

### <span data-ttu-id="b13b0-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b13b0-111">-Name</span></span>
<span data-ttu-id="b13b0-112">Określa nazwę wdrożenia zarządzania interfejsem API, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b13b0-112">Specifies the name of the API Management deployment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b13b0-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b13b0-113">-PassThru</span></span>
<span data-ttu-id="b13b0-114">Wskazuje, że to polecenie cmdlet zwraca wartość $True, jeśli operacja się powiedzie.</span><span class="sxs-lookup"><span data-stu-id="b13b0-114">Indicates that this cmdlet returns a value of $True if the operation succeeds.</span></span>

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

### <span data-ttu-id="b13b0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b13b0-115">-ResourceGroupName</span></span>
<span data-ttu-id="b13b0-116">Określa nazwę grupy zasobów, w której istnieje wdrożenie zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="b13b0-116">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

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

### <span data-ttu-id="b13b0-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b13b0-117">-Confirm</span></span>
<span data-ttu-id="b13b0-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b13b0-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b13b0-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b13b0-119">-WhatIf</span></span>
<span data-ttu-id="b13b0-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b13b0-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b13b0-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b13b0-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b13b0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b13b0-122">-DefaultProfile</span></span>
<span data-ttu-id="b13b0-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b13b0-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b13b0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b13b0-124">CommonParameters</span></span>
<span data-ttu-id="b13b0-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b13b0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b13b0-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b13b0-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b13b0-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b13b0-127">INPUTS</span></span>

## <span data-ttu-id="b13b0-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b13b0-128">OUTPUTS</span></span>

### <span data-ttu-id="b13b0-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b13b0-129">System.Boolean</span></span>

## <span data-ttu-id="b13b0-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b13b0-130">NOTES</span></span>

## <span data-ttu-id="b13b0-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b13b0-131">RELATED LINKS</span></span>

[<span data-ttu-id="b13b0-132">Backup-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="b13b0-132">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="b13b0-133">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="b13b0-133">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="b13b0-134">Nowe — AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="b13b0-134">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="b13b0-135">Restore-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="b13b0-135">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)


