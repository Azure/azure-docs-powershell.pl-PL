---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 8FB2D9A0-BF7A-482D-B3A2-566FCA8C62A1
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/reset-azpowerbiworkspacecollectionaccesskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Reset-AzPowerBIWorkspaceCollectionAccessKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Reset-AzPowerBIWorkspaceCollectionAccessKey.md
ms.openlocfilehash: d9e30c81eb0e2422b91be79bcfc7c732291c30cb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98500153"
---
# <span data-ttu-id="bdb80-101">Reset-AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="bdb80-101">Reset-AzPowerBIWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="bdb80-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bdb80-102">SYNOPSIS</span></span>
<span data-ttu-id="bdb80-103">Resetowanie określonego klawisza dostępu.</span><span class="sxs-lookup"><span data-stu-id="bdb80-103">Resets the specified access key.</span></span>

## <span data-ttu-id="bdb80-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bdb80-104">SYNTAX</span></span>

```
Reset-AzPowerBIWorkspaceCollectionAccessKey [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-Key1] [-Key2] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bdb80-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bdb80-105">DESCRIPTION</span></span>
<span data-ttu-id="bdb80-106">Polecenie cmdlet **Reseting-AzPowerBIWorkspaceCollectionAccessKey** umożliwia resetowanie określonego klucza dostępu w kolekcji obszaru roboczego usługi Power BI.</span><span class="sxs-lookup"><span data-stu-id="bdb80-106">The **Reset-AzPowerBIWorkspaceCollectionAccessKey** cmdlet resets the specified access key in your Power BI workspace collection.</span></span>

## <span data-ttu-id="bdb80-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bdb80-107">EXAMPLES</span></span>

### <span data-ttu-id="bdb80-108">Przykład 1: Resetowanie podstawowego klucza dostępu</span><span class="sxs-lookup"><span data-stu-id="bdb80-108">Example 1: Reset the primary access key</span></span>
```
PS C:\>Reset-AzPowerBIWorkspaceCollectionAccessKey -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11" -Key1
```

<span data-ttu-id="bdb80-109">To polecenie resetuje podstawowy klucz dostępu do kolekcji obszarów roboczych o nazwie WCN11 w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="bdb80-109">This command resets the primary access key for the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="bdb80-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bdb80-110">PARAMETERS</span></span>

### <span data-ttu-id="bdb80-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdb80-111">-DefaultProfile</span></span>
<span data-ttu-id="bdb80-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="bdb80-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bdb80-113">-Key1</span><span class="sxs-lookup"><span data-stu-id="bdb80-113">-Key1</span></span>
<span data-ttu-id="bdb80-114">Wskazuje, że ten aplet polecenia resetuje podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="bdb80-114">Indicates that this cmdlet resets the primary access key.</span></span>

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

### <span data-ttu-id="bdb80-115">-Key2</span><span class="sxs-lookup"><span data-stu-id="bdb80-115">-Key2</span></span>
<span data-ttu-id="bdb80-116">Wskazuje, że ten aplet polecenia resetuje pomocniczy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="bdb80-116">Indicates that this cmdlet resets the secondary access key.</span></span>

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

### <span data-ttu-id="bdb80-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdb80-117">-ResourceGroupName</span></span>
<span data-ttu-id="bdb80-118">Określa nazwę grupy zasobów kolekcji.</span><span class="sxs-lookup"><span data-stu-id="bdb80-118">Specifies the name of the resource group of the collection.</span></span>

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

### <span data-ttu-id="bdb80-119">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="bdb80-119">-WorkspaceCollectionName</span></span>
<span data-ttu-id="bdb80-120">Określa nazwę kolekcji obszaru roboczego usługi Power BI, na której działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bdb80-120">Specifies the name of the Power BI workspace collection on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="bdb80-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bdb80-121">-Confirm</span></span>
<span data-ttu-id="bdb80-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bdb80-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdb80-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdb80-123">-WhatIf</span></span>
<span data-ttu-id="bdb80-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bdb80-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bdb80-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bdb80-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdb80-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdb80-126">CommonParameters</span></span>
<span data-ttu-id="bdb80-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdb80-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdb80-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdb80-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdb80-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bdb80-129">INPUTS</span></span>

### <span data-ttu-id="bdb80-130">System. String</span><span class="sxs-lookup"><span data-stu-id="bdb80-130">System.String</span></span>

## <span data-ttu-id="bdb80-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bdb80-131">OUTPUTS</span></span>

### <span data-ttu-id="bdb80-132">Microsoft. Azure. Commands. Management. PowerBIEmbedded. models. PSWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="bdb80-132">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="bdb80-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bdb80-133">NOTES</span></span>

## <span data-ttu-id="bdb80-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bdb80-134">RELATED LINKS</span></span>

[<span data-ttu-id="bdb80-135">Get-AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="bdb80-135">Get-AzPowerBIWorkspaceCollectionAccessKey</span></span>](./Get-AzPowerBIWorkspaceCollectionAccessKey.md)


