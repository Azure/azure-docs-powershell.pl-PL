---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 585D6C4D-EA80-4E6B-8C36-E7632430431F
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreAccount.md
ms.openlocfilehash: 75af40b104bbf6ffa65211087572140a070b71e8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94305586"
---
# <span data-ttu-id="035be-101">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="035be-101">Remove-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="035be-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="035be-102">SYNOPSIS</span></span>
<span data-ttu-id="035be-103">Trwale usuwa konto Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="035be-103">Deletes a Data Lake Store account permanently.</span></span>

## <span data-ttu-id="035be-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="035be-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="035be-105">Opis</span><span class="sxs-lookup"><span data-stu-id="035be-105">DESCRIPTION</span></span>
<span data-ttu-id="035be-106">Polecenie cmdlet **Remove-AzDataLakeStoreAccount** umożliwia trwałe usunięcie konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="035be-106">The **Remove-AzDataLakeStoreAccount** cmdlet deletes a Data Lake Store account permanently.</span></span>

## <span data-ttu-id="035be-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="035be-107">EXAMPLES</span></span>

### <span data-ttu-id="035be-108">Przykład 1. Usuń konto w usłudze Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="035be-108">Example 1: Remove a Data Lake Store account</span></span>
```
PS C:\>Remove-AzDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="035be-109">To polecenie usuwa konto o nazwie ContosoADL z usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="035be-109">This command removes the account named ContosoADL from the Data Lake Store.</span></span>

## <span data-ttu-id="035be-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="035be-110">PARAMETERS</span></span>

### <span data-ttu-id="035be-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="035be-111">-DefaultProfile</span></span>
<span data-ttu-id="035be-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="035be-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="035be-113">-Force</span><span class="sxs-lookup"><span data-stu-id="035be-113">-Force</span></span>
<span data-ttu-id="035be-114">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="035be-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="035be-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="035be-115">-Name</span></span>
<span data-ttu-id="035be-116">Określa nazwę konta, które ma zostać usunięte.</span><span class="sxs-lookup"><span data-stu-id="035be-116">Specifies the name of the account to remove.</span></span>

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

### <span data-ttu-id="035be-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="035be-117">-PassThru</span></span>
<span data-ttu-id="035be-118">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="035be-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="035be-119">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="035be-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="035be-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="035be-120">-ResourceGroupName</span></span>
<span data-ttu-id="035be-121">Określa grupę zasobów zawierającą konto do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="035be-121">Specifies the resource group that contains the account to remove.</span></span>

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

### <span data-ttu-id="035be-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="035be-122">-Confirm</span></span>
<span data-ttu-id="035be-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="035be-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="035be-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="035be-124">-WhatIf</span></span>
<span data-ttu-id="035be-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="035be-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="035be-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="035be-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="035be-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="035be-127">CommonParameters</span></span>
<span data-ttu-id="035be-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="035be-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="035be-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="035be-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="035be-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="035be-130">INPUTS</span></span>

### <span data-ttu-id="035be-131">System. String</span><span class="sxs-lookup"><span data-stu-id="035be-131">System.String</span></span>

## <span data-ttu-id="035be-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="035be-132">OUTPUTS</span></span>

### <span data-ttu-id="035be-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="035be-133">System.Boolean</span></span>

## <span data-ttu-id="035be-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="035be-134">NOTES</span></span>

## <span data-ttu-id="035be-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="035be-135">RELATED LINKS</span></span>

[<span data-ttu-id="035be-136">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="035be-136">Get-AzDataLakeStoreAccount</span></span>](./Get-AzDataLakeStoreAccount.md)

[<span data-ttu-id="035be-137">Nowe — AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="035be-137">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="035be-138">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="035be-138">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

[<span data-ttu-id="035be-139">Test — AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="035be-139">Test-AzDataLakeStoreAccount</span></span>](./Test-AzDataLakeStoreAccount.md)


