---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 8FB2D9A0-BF7A-482D-B3A2-566FCA8C62A1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/reset-azurermpowerbiworkspacecollectionaccesskeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys.md
ms.openlocfilehash: cb8236acfc0fd1d349091593a2510da271820020
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719073"
---
# <span data-ttu-id="70c1c-101">Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys</span><span class="sxs-lookup"><span data-stu-id="70c1c-101">Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys</span></span>

## <span data-ttu-id="70c1c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="70c1c-102">SYNOPSIS</span></span>
<span data-ttu-id="70c1c-103">Resetowanie określonego klawisza dostępu.</span><span class="sxs-lookup"><span data-stu-id="70c1c-103">Resets the specified access key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="70c1c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="70c1c-104">SYNTAX</span></span>

```
Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys [-ResourceGroupName] <String>
 [-WorkspaceCollectionName] <String> [-Key1] [-Key2] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70c1c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="70c1c-105">DESCRIPTION</span></span>
<span data-ttu-id="70c1c-106">Polecenie cmdlet **Reseting-AzureRmPowerBIWorkspaceCollectionAccessKeys** umożliwia resetowanie określonego klucza dostępu w kolekcji obszaru roboczego usługi Power BI.</span><span class="sxs-lookup"><span data-stu-id="70c1c-106">The **Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys** cmdlet resets the specified access key in your Power BI workspace collection.</span></span>

## <span data-ttu-id="70c1c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="70c1c-107">EXAMPLES</span></span>

### <span data-ttu-id="70c1c-108">Przykład 1: Resetowanie podstawowego klucza dostępu</span><span class="sxs-lookup"><span data-stu-id="70c1c-108">Example 1: Reset the primary access key</span></span>
```
PS C:\>Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11" -Key1
```

<span data-ttu-id="70c1c-109">To polecenie resetuje podstawowy klucz dostępu do kolekcji obszarów roboczych o nazwie WCN11 w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="70c1c-109">This command resets the primary access key for the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="70c1c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="70c1c-110">PARAMETERS</span></span>

### <span data-ttu-id="70c1c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70c1c-111">-DefaultProfile</span></span>
<span data-ttu-id="70c1c-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="70c1c-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="70c1c-113">-Key1</span><span class="sxs-lookup"><span data-stu-id="70c1c-113">-Key1</span></span>
<span data-ttu-id="70c1c-114">Wskazuje, że ten aplet polecenia resetuje podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="70c1c-114">Indicates that this cmdlet resets the primary access key.</span></span>

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

### <span data-ttu-id="70c1c-115">-Key2</span><span class="sxs-lookup"><span data-stu-id="70c1c-115">-Key2</span></span>
<span data-ttu-id="70c1c-116">Wskazuje, że ten aplet polecenia resetuje pomocniczy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="70c1c-116">Indicates that this cmdlet resets the secondary access key.</span></span>

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

### <span data-ttu-id="70c1c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70c1c-117">-ResourceGroupName</span></span>
<span data-ttu-id="70c1c-118">Określa nazwę grupy zasobów kolekcji.</span><span class="sxs-lookup"><span data-stu-id="70c1c-118">Specifies the name of the resource group of the collection.</span></span>

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

### <span data-ttu-id="70c1c-119">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="70c1c-119">-WorkspaceCollectionName</span></span>
<span data-ttu-id="70c1c-120">Określa nazwę kolekcji obszaru roboczego usługi Power BI, na której działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70c1c-120">Specifies the name of the Power BI workspace collection on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70c1c-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="70c1c-121">-Confirm</span></span>
<span data-ttu-id="70c1c-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70c1c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70c1c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70c1c-123">-WhatIf</span></span>
<span data-ttu-id="70c1c-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70c1c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70c1c-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="70c1c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70c1c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70c1c-126">CommonParameters</span></span>
<span data-ttu-id="70c1c-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70c1c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70c1c-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70c1c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70c1c-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="70c1c-129">INPUTS</span></span>

### <span data-ttu-id="70c1c-130">System. String</span><span class="sxs-lookup"><span data-stu-id="70c1c-130">System.String</span></span>

## <span data-ttu-id="70c1c-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="70c1c-131">OUTPUTS</span></span>

### <span data-ttu-id="70c1c-132">Microsoft. Azure. Commands. Management. PowerBIEmbedded. models. PSWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="70c1c-132">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="70c1c-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="70c1c-133">NOTES</span></span>

## <span data-ttu-id="70c1c-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="70c1c-134">RELATED LINKS</span></span>

[<span data-ttu-id="70c1c-135">Get-AzureRmPowerBIWorkspaceCollectionAccessKeys</span><span class="sxs-lookup"><span data-stu-id="70c1c-135">Get-AzureRmPowerBIWorkspaceCollectionAccessKeys</span></span>](./Get-AzureRmPowerBIWorkspaceCollectionAccessKeys.md)


