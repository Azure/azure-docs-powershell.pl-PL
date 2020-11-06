---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: A4A8D996-72A2-4154-98DA-5F84CAA010B9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOperation.md
ms.openlocfilehash: 685da9955f272066ec39890ea0f3a063d3b2f9b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527746"
---
# <span data-ttu-id="b128d-101">Remove-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="b128d-101">Remove-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="b128d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b128d-102">SYNOPSIS</span></span>
<span data-ttu-id="b128d-103">Usuwa istniejącą operację.</span><span class="sxs-lookup"><span data-stu-id="b128d-103">Removes an existing operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b128d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b128d-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b128d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b128d-105">DESCRIPTION</span></span>
<span data-ttu-id="b128d-106">Polecenie cmdlet **Remove-AzureRmApiManagementOperation** Usuwa istniejącą operację.</span><span class="sxs-lookup"><span data-stu-id="b128d-106">The **Remove-AzureRmApiManagementOperation** cmdlet removes an existing operation.</span></span>

## <span data-ttu-id="b128d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b128d-107">EXAMPLES</span></span>

### <span data-ttu-id="b128d-108">Przykład 1. Usuń istniejącą operację interfejsu API</span><span class="sxs-lookup"><span data-stu-id="b128d-108">Example 1: Remove an existing API Operation</span></span>
```
PS C:\>Remove-AzureRmApiManagementOperation -Context $APImContext -ApiId "0123456789" -OperationId "9876543210" -Force
```

<span data-ttu-id="b128d-109">To polecenie usuwa istniejącą operację interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="b128d-109">This command removes an existing API Operation.</span></span>

## <span data-ttu-id="b128d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b128d-110">PARAMETERS</span></span>

### <span data-ttu-id="b128d-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="b128d-111">-ApiId</span></span>
<span data-ttu-id="b128d-112">Określa identyfikator interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="b128d-112">Specifies the identifier of the API.</span></span>

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

### <span data-ttu-id="b128d-113">-Context</span><span class="sxs-lookup"><span data-stu-id="b128d-113">-Context</span></span>
<span data-ttu-id="b128d-114">Określa wystąpienie **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="b128d-114">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="b128d-115">-OperationId</span><span class="sxs-lookup"><span data-stu-id="b128d-115">-OperationId</span></span>
<span data-ttu-id="b128d-116">Określa identyfikator operacji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="b128d-116">Specifies the identifier of the API operation.</span></span>

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

### <span data-ttu-id="b128d-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b128d-117">-PassThru</span></span>
<span data-ttu-id="b128d-118">Wskazuje, że to polecenie cmdlet zwraca wartość $True, jeśli ta operacja się powiedzie lub wartość $False w przeciwnym razie.</span><span class="sxs-lookup"><span data-stu-id="b128d-118">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="b128d-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b128d-119">-Confirm</span></span>
<span data-ttu-id="b128d-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b128d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b128d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b128d-121">-WhatIf</span></span>
<span data-ttu-id="b128d-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b128d-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b128d-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b128d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b128d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b128d-124">-DefaultProfile</span></span>
<span data-ttu-id="b128d-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b128d-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b128d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b128d-126">CommonParameters</span></span>
<span data-ttu-id="b128d-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b128d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b128d-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b128d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b128d-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b128d-129">INPUTS</span></span>

## <span data-ttu-id="b128d-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b128d-130">OUTPUTS</span></span>

### <span data-ttu-id="b128d-131">logiczną</span><span class="sxs-lookup"><span data-stu-id="b128d-131">bool</span></span>

## <span data-ttu-id="b128d-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b128d-132">NOTES</span></span>

## <span data-ttu-id="b128d-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b128d-133">RELATED LINKS</span></span>

[<span data-ttu-id="b128d-134">Get-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="b128d-134">Get-AzureRmApiManagementOperation</span></span>](./Get-AzureRmApiManagementOperation.md)

[<span data-ttu-id="b128d-135">Nowe — AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="b128d-135">New-AzureRmApiManagementOperation</span></span>](./New-AzureRmApiManagementOperation.md)

[<span data-ttu-id="b128d-136">Set-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="b128d-136">Set-AzureRmApiManagementOperation</span></span>](./Set-AzureRmApiManagementOperation.md)


