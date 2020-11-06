---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/remove-azurermanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Remove-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Remove-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 4976c34437b2f858f8e76924754fe04a8b1e0a84
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547719"
---
# <span data-ttu-id="dfe14-101">Remove-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="dfe14-101">Remove-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="dfe14-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dfe14-102">SYNOPSIS</span></span>
<span data-ttu-id="dfe14-103">Usuwanie wystąpienia serwera usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="dfe14-103">Deletes an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dfe14-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dfe14-104">SYNTAX</span></span>

```
Remove-AzureRmAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dfe14-105">Opis</span><span class="sxs-lookup"><span data-stu-id="dfe14-105">DESCRIPTION</span></span>
<span data-ttu-id="dfe14-106">Polecenie cmdlet Remove-AzureRmAnalysisServicesServer powoduje usunięcie wystąpienia serwera usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="dfe14-106">The Remove-AzureRmAnalysisServicesServer cmdlet  deletes an instance of Analysis Services server</span></span>

## <span data-ttu-id="dfe14-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dfe14-107">EXAMPLES</span></span>

### <span data-ttu-id="dfe14-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="dfe14-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="dfe14-109">To polecenie usunie serwer o nazwie TestServer w ramach testera zasobów.</span><span class="sxs-lookup"><span data-stu-id="dfe14-109">This command will remove the server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="dfe14-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dfe14-110">PARAMETERS</span></span>

### <span data-ttu-id="dfe14-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfe14-111">-DefaultProfile</span></span>
<span data-ttu-id="dfe14-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dfe14-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dfe14-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="dfe14-113">-Name</span></span>
<span data-ttu-id="dfe14-114">Nazwa serwera usług Analysis Services</span><span class="sxs-lookup"><span data-stu-id="dfe14-114">Name of the Analysis Services server</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dfe14-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dfe14-115">-PassThru</span></span>
<span data-ttu-id="dfe14-116">Po pomyślnym zakończeniu operacji zwróci dane usuniętego serwera.</span><span class="sxs-lookup"><span data-stu-id="dfe14-116">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="dfe14-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfe14-117">-ResourceGroupName</span></span>
<span data-ttu-id="dfe14-118">Nazwa grupy zasobów platformy Azure, do której należy serwer</span><span class="sxs-lookup"><span data-stu-id="dfe14-118">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dfe14-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dfe14-119">-Confirm</span></span>
<span data-ttu-id="dfe14-120">Monituje użytkownika o potwierdzenie, czy wykonać operację.</span><span class="sxs-lookup"><span data-stu-id="dfe14-120">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="dfe14-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfe14-121">-WhatIf</span></span>
<span data-ttu-id="dfe14-122">Opisuje akcje, które zostaną wykonane przez bieżącą operację bez ich rzeczywistego wykonywania.</span><span class="sxs-lookup"><span data-stu-id="dfe14-122">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="dfe14-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfe14-123">CommonParameters</span></span>
<span data-ttu-id="dfe14-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfe14-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfe14-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfe14-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfe14-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dfe14-126">INPUTS</span></span>

### <span data-ttu-id="dfe14-127">System. String</span><span class="sxs-lookup"><span data-stu-id="dfe14-127">System.String</span></span>

## <span data-ttu-id="dfe14-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dfe14-128">OUTPUTS</span></span>

### <span data-ttu-id="dfe14-129">Microsoft. Azure. Commands. AnalysisServices. models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="dfe14-129">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="dfe14-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dfe14-130">NOTES</span></span>
<span data-ttu-id="dfe14-131">Alias: Remove-AzureAs</span><span class="sxs-lookup"><span data-stu-id="dfe14-131">Alias: Remove-AzureAs</span></span>

## <span data-ttu-id="dfe14-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dfe14-132">RELATED LINKS</span></span>

[<span data-ttu-id="dfe14-133">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="dfe14-133">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="dfe14-134">Nowe — AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="dfe14-134">New-AzureRmAnalysisServicesServer</span></span>](./New-AzureRmAnalysisServicesServer.md)
