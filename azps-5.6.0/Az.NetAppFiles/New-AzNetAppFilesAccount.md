---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/new-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesAccount.md
ms.openlocfilehash: 588952f9f3aa0cb9c7351ee862ad6db82d66f85d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968497"
---
# <span data-ttu-id="10e43-101">New-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="10e43-101">New-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="10e43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10e43-102">SYNOPSIS</span></span>
<span data-ttu-id="10e43-103">Tworzy nowe konto usługi Azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="10e43-103">Creates a new Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="10e43-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="10e43-104">SYNTAX</span></span>

```
New-AzNetAppFilesAccount -ResourceGroupName <String> -Location <String> -Name <String>
 [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10e43-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="10e43-105">DESCRIPTION</span></span>
<span data-ttu-id="10e43-106">Polecenie **cmdlet New-AzNetAppFilesAccount** tworzy konto ANF.</span><span class="sxs-lookup"><span data-stu-id="10e43-106">The **New-AzNetAppFilesAccount** cmdlet creates an ANF account.</span></span>

## <span data-ttu-id="10e43-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="10e43-107">EXAMPLES</span></span>

### <span data-ttu-id="10e43-108">Przykład 1. Tworzenie konta ANF</span><span class="sxs-lookup"><span data-stu-id="10e43-108">Example 1: Create an ANF account</span></span>
```
PS C:\>New-AzNetAppFilesAccount -ResourceGroupName "MyRG" -Name "MyAnfAccount" -l "westus2"

Output:

Location          : westus2
Id                : /subscriptions/mySubs/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount
Name              : MyAnfAccount
Type              : Microsoft.NetApp/netAppAccounts
Tags              :
ProvisioningState : Succeeded
```

<span data-ttu-id="10e43-109">To polecenie tworzy nowe konto ANF "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="10e43-109">This command creates the new ANF account "MyAnfAccount".</span></span>

## <span data-ttu-id="10e43-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="10e43-110">PARAMETERS</span></span>

### <span data-ttu-id="10e43-111">-ActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="10e43-111">-ActiveDirectory</span></span>
<span data-ttu-id="10e43-112">Tablica z hasztagami reprezentująca aktywne katalogi</span><span class="sxs-lookup"><span data-stu-id="10e43-112">A hashtable array which represents the active directories</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10e43-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10e43-113">-DefaultProfile</span></span>
<span data-ttu-id="10e43-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="10e43-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10e43-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="10e43-115">-Location</span></span>
<span data-ttu-id="10e43-116">Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="10e43-116">The location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10e43-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="10e43-117">-Name</span></span>
<span data-ttu-id="10e43-118">Nazwa konta ANF</span><span class="sxs-lookup"><span data-stu-id="10e43-118">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10e43-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10e43-119">-ResourceGroupName</span></span>
<span data-ttu-id="10e43-120">Grupa zasobów konta ANF</span><span class="sxs-lookup"><span data-stu-id="10e43-120">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10e43-121">— Tag</span><span class="sxs-lookup"><span data-stu-id="10e43-121">-Tag</span></span>
<span data-ttu-id="10e43-122">Tabela skrótów reprezentująca tagi zasobów</span><span class="sxs-lookup"><span data-stu-id="10e43-122">A hashtable which represents resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10e43-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="10e43-123">-Confirm</span></span>
<span data-ttu-id="10e43-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="10e43-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10e43-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10e43-125">-WhatIf</span></span>
<span data-ttu-id="10e43-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10e43-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10e43-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="10e43-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10e43-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10e43-128">CommonParameters</span></span>
<span data-ttu-id="10e43-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10e43-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10e43-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="10e43-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10e43-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="10e43-131">INPUTS</span></span>

### <span data-ttu-id="10e43-132">Brak</span><span class="sxs-lookup"><span data-stu-id="10e43-132">None</span></span>

## <span data-ttu-id="10e43-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="10e43-133">OUTPUTS</span></span>

### <span data-ttu-id="10e43-134">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="10e43-134">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="10e43-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="10e43-135">NOTES</span></span>

## <span data-ttu-id="10e43-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="10e43-136">RELATED LINKS</span></span>
