---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: C2CC10DE-1D36-4937-8A3E-9776BE80DF9A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementAuthorizationServer.md
ms.openlocfilehash: 16a48b6f945aac8ef287ff612d64da1273add521
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525782"
---
# <span data-ttu-id="3c300-101">Remove-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="3c300-101">Remove-AzureRmApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="3c300-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3c300-102">SYNOPSIS</span></span>
<span data-ttu-id="3c300-103">Usuwa serwer autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="3c300-103">Removes an authorization server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3c300-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3c300-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext> -ServerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c300-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3c300-105">DESCRIPTION</span></span>
<span data-ttu-id="3c300-106">Polecenie cmdlet **Remove-AzureRmApiManagementAuthorizationServer** usuwa serwer autoryzacji zarządzania interfejsem Azure API.</span><span class="sxs-lookup"><span data-stu-id="3c300-106">The **Remove-AzureRmApiManagementAuthorizationServer** cmdlet removes an Azure API Management authorization server.</span></span>

## <span data-ttu-id="3c300-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3c300-107">EXAMPLES</span></span>

## <span data-ttu-id="3c300-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3c300-108">PARAMETERS</span></span>

### <span data-ttu-id="3c300-109">-Context</span><span class="sxs-lookup"><span data-stu-id="3c300-109">-Context</span></span>
<span data-ttu-id="3c300-110">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="3c300-110">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="3c300-111">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3c300-111">-PassThru</span></span>
<span data-ttu-id="3c300-112">passthru</span><span class="sxs-lookup"><span data-stu-id="3c300-112">passthru</span></span>

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

### <span data-ttu-id="3c300-113">-ServerId</span><span class="sxs-lookup"><span data-stu-id="3c300-113">-ServerId</span></span>
<span data-ttu-id="3c300-114">Określa identyfikator serwera autoryzacji, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="3c300-114">Specifies the ID of the authorization server to remove.</span></span>

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

### <span data-ttu-id="3c300-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3c300-115">-Confirm</span></span>
<span data-ttu-id="3c300-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c300-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c300-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c300-117">-WhatIf</span></span>
<span data-ttu-id="3c300-118">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c300-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c300-119">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3c300-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c300-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c300-120">-DefaultProfile</span></span>
<span data-ttu-id="3c300-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3c300-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c300-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c300-122">CommonParameters</span></span>
<span data-ttu-id="3c300-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c300-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c300-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c300-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c300-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3c300-125">INPUTS</span></span>

## <span data-ttu-id="3c300-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3c300-126">OUTPUTS</span></span>

### <span data-ttu-id="3c300-127">Wartość</span><span class="sxs-lookup"><span data-stu-id="3c300-127">Boolean</span></span>

## <span data-ttu-id="3c300-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3c300-128">NOTES</span></span>

## <span data-ttu-id="3c300-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3c300-129">RELATED LINKS</span></span>

[<span data-ttu-id="3c300-130">Get-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="3c300-130">Get-AzureRmApiManagementAuthorizationServer</span></span>](./Get-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="3c300-131">Nowe — AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="3c300-131">New-AzureRmApiManagementAuthorizationServer</span></span>](./New-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="3c300-132">Set-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="3c300-132">Set-AzureRmApiManagementAuthorizationServer</span></span>](./Set-AzureRmApiManagementAuthorizationServer.md)


