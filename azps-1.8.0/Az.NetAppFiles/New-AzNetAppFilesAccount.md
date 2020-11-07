---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesAccount.md
ms.openlocfilehash: 87febe648a845d595f35c1a14b024fbd97824be1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709742"
---
# <span data-ttu-id="cfa60-101">New-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="cfa60-101">New-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="cfa60-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cfa60-102">SYNOPSIS</span></span>
<span data-ttu-id="cfa60-103">Tworzy nowe konto usługi Azure NetApp plików (ANF).</span><span class="sxs-lookup"><span data-stu-id="cfa60-103">Creates a new Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="cfa60-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cfa60-104">SYNTAX</span></span>

```
New-AzNetAppFilesAccount -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cfa60-105">Opis</span><span class="sxs-lookup"><span data-stu-id="cfa60-105">DESCRIPTION</span></span>
<span data-ttu-id="cfa60-106">Polecenie cmdlet **New-AzNetAppFilesAccount** tworzy konto ANF.</span><span class="sxs-lookup"><span data-stu-id="cfa60-106">The **New-AzNetAppFilesAccount** cmdlet creates an ANF account.</span></span>

## <span data-ttu-id="cfa60-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cfa60-107">EXAMPLES</span></span>

### <span data-ttu-id="cfa60-108">Przykład 1. Tworzenie konta ANF</span><span class="sxs-lookup"><span data-stu-id="cfa60-108">Example 1: Create an ANF account</span></span>
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

<span data-ttu-id="cfa60-109">To polecenie tworzy nowe konto ANF "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="cfa60-109">This command creates the new ANF account "MyAnfAccount".</span></span>

## <span data-ttu-id="cfa60-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cfa60-110">PARAMETERS</span></span>

### <span data-ttu-id="cfa60-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfa60-111">-DefaultProfile</span></span>
<span data-ttu-id="cfa60-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cfa60-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfa60-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="cfa60-113">-Location</span></span>
<span data-ttu-id="cfa60-114">Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="cfa60-114">The location of the resource</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfa60-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cfa60-115">-Name</span></span>
<span data-ttu-id="cfa60-116">Nazwa konta usługi ANF</span><span class="sxs-lookup"><span data-stu-id="cfa60-116">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfa60-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfa60-117">-ResourceGroupName</span></span>
<span data-ttu-id="cfa60-118">Grupa zasobów konta ANF</span><span class="sxs-lookup"><span data-stu-id="cfa60-118">The resource group of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfa60-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="cfa60-119">-Tag</span></span>
<span data-ttu-id="cfa60-120">Obiekt Hashtable reprezentujący znaczniki zasobów</span><span class="sxs-lookup"><span data-stu-id="cfa60-120">A hashtable which represents resource tags</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfa60-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cfa60-121">-Confirm</span></span>
<span data-ttu-id="cfa60-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cfa60-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfa60-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cfa60-123">-WhatIf</span></span>
<span data-ttu-id="cfa60-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cfa60-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cfa60-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cfa60-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfa60-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfa60-126">CommonParameters</span></span>
<span data-ttu-id="cfa60-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfa60-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="cfa60-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfa60-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfa60-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cfa60-129">INPUTS</span></span>

### <span data-ttu-id="cfa60-130">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="cfa60-130">None</span></span>

## <span data-ttu-id="cfa60-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cfa60-131">OUTPUTS</span></span>

### <span data-ttu-id="cfa60-132">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="cfa60-132">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="cfa60-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cfa60-133">NOTES</span></span>

## <span data-ttu-id="cfa60-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cfa60-134">RELATED LINKS</span></span>
