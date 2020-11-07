---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 1B29AB8C-95DD-4C4F-86E2-2F81E8020CEA
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragetable
schema: 2.0.0
ms.openlocfilehash: e33e32051c15483956d0764f5e9ddca25a083f23
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899161"
---
# <span data-ttu-id="a30c1-101">Remove-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="a30c1-101">Remove-AzureStorageTable</span></span>

## <span data-ttu-id="a30c1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a30c1-102">SYNOPSIS</span></span>
<span data-ttu-id="a30c1-103">Usuwa tabelę magazynu.</span><span class="sxs-lookup"><span data-stu-id="a30c1-103">Removes a storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a30c1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a30c1-104">SYNTAX</span></span>

```
Remove-AzureStorageTable [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a30c1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a30c1-105">DESCRIPTION</span></span>
<span data-ttu-id="a30c1-106">Polecenie cmdlet **Remove-AzureStorageTable** usuwa co najmniej jeden magazyn z konta magazynu na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="a30c1-106">The **Remove-AzureStorageTable** cmdlet removes one or more storage tables from a storage account in Azure.</span></span>

## <span data-ttu-id="a30c1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a30c1-107">EXAMPLES</span></span>

### <span data-ttu-id="a30c1-108">Przykład 1. Usuwanie tabeli</span><span class="sxs-lookup"><span data-stu-id="a30c1-108">Example 1: Remove a table</span></span>
```
PS C:\>Remove-AzureStorageTable -Name "TableABC"
```

<span data-ttu-id="a30c1-109">To polecenie umożliwia usunięcie tabeli.</span><span class="sxs-lookup"><span data-stu-id="a30c1-109">This command removes a table.</span></span>

### <span data-ttu-id="a30c1-110">Przykład 2: Usuwanie kilku tabel</span><span class="sxs-lookup"><span data-stu-id="a30c1-110">Example 2: Remove several tables</span></span>
```
PS C:\>Get-AzureStorageTable table* | Remove-AzureStorageTable
```

<span data-ttu-id="a30c1-111">W tym przykładzie użyto symbolu wieloznacznego z parametrem *name* w celu uzyskania wszystkich tabel pasujących do tabeli wzorzec, a następnie przekazanie wyniku w potoku w celu usunięcia tabel.</span><span class="sxs-lookup"><span data-stu-id="a30c1-111">This example uses a wildcard character with the *Name* parameter to get all tables that match the pattern table and then passes the result on the pipeline to remove the tables.</span></span>

## <span data-ttu-id="a30c1-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a30c1-112">PARAMETERS</span></span>

### <span data-ttu-id="a30c1-113">-Context</span><span class="sxs-lookup"><span data-stu-id="a30c1-113">-Context</span></span>
<span data-ttu-id="a30c1-114">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="a30c1-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="a30c1-115">Możesz ją utworzyć przy użyciu polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="a30c1-115">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a30c1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a30c1-116">-DefaultProfile</span></span>
<span data-ttu-id="a30c1-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a30c1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a30c1-118">-Force</span><span class="sxs-lookup"><span data-stu-id="a30c1-118">-Force</span></span>
<span data-ttu-id="a30c1-119">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="a30c1-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a30c1-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a30c1-120">-Name</span></span>
<span data-ttu-id="a30c1-121">Określa nazwę tabeli, która ma zostać usunięta.</span><span class="sxs-lookup"><span data-stu-id="a30c1-121">Specifies the name of the table to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a30c1-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a30c1-122">-PassThru</span></span>
<span data-ttu-id="a30c1-123">Wskazuje, że to polecenie cmdlet zwraca **wartość logiczną** odzwierciedlającą sukces operacji.</span><span class="sxs-lookup"><span data-stu-id="a30c1-123">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="a30c1-124">Domyślnie to polecenie cmdlet nie zwraca wartości.</span><span class="sxs-lookup"><span data-stu-id="a30c1-124">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="a30c1-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a30c1-125">-Confirm</span></span>
<span data-ttu-id="a30c1-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a30c1-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a30c1-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a30c1-127">-WhatIf</span></span>
<span data-ttu-id="a30c1-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a30c1-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a30c1-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a30c1-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a30c1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a30c1-130">CommonParameters</span></span>
<span data-ttu-id="a30c1-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a30c1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a30c1-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a30c1-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a30c1-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a30c1-133">INPUTS</span></span>

### <span data-ttu-id="a30c1-134">System. String</span><span class="sxs-lookup"><span data-stu-id="a30c1-134">System.String</span></span>

### <span data-ttu-id="a30c1-135">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a30c1-135">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a30c1-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a30c1-136">OUTPUTS</span></span>

### <span data-ttu-id="a30c1-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a30c1-137">System.Boolean</span></span>

## <span data-ttu-id="a30c1-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a30c1-138">NOTES</span></span>

## <span data-ttu-id="a30c1-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a30c1-139">RELATED LINKS</span></span>

[<span data-ttu-id="a30c1-140">Get-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="a30c1-140">Get-AzureStorageTable</span></span>](./Get-AzureStorageTable.md)
