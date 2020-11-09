---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: C6BB6E4D-6009-4796-866B-17115FDFA06D
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticscatalogcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: 9fbc00fe190e0a53fc9c41a6894ec35a7f8d9129
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94305808"
---
# <span data-ttu-id="9cd3a-101">Remove-AzDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="9cd3a-101">Remove-AzDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="9cd3a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9cd3a-102">SYNOPSIS</span></span>
<span data-ttu-id="9cd3a-103">Usuwa poświadczenia usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="9cd3a-103">Deletes an Azure Data Lake Analytics credential.</span></span>

## <span data-ttu-id="9cd3a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9cd3a-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String> [-Name] <String>
 [[-Password] <PSCredential>] [-Recurse] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9cd3a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9cd3a-105">DESCRIPTION</span></span>
<span data-ttu-id="9cd3a-106">Polecenie cmdlet Remove-AzDataLakeAnalyticsCatalogCredential usuwa poświadczenia wykazu usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="9cd3a-106">The Remove-AzDataLakeAnalyticsCatalogCredential cmdlet deletes an Azure Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="9cd3a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9cd3a-107">EXAMPLES</span></span>

### <span data-ttu-id="9cd3a-108">Przykład 1: usuwanie poświadczenia</span><span class="sxs-lookup"><span data-stu-id="9cd3a-108">Example 1: Remove a credential</span></span>
```
PS C:\> Remove-AzDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdla" `
                      -DatabaseName "DatabaseName" `
                      -Name "CredName"
```

<span data-ttu-id="9cd3a-109">To polecenie usuwa określone poświadczenia wykazu usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="9cd3a-109">This command removes the specified Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="9cd3a-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9cd3a-110">PARAMETERS</span></span>

### <span data-ttu-id="9cd3a-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="9cd3a-111">-Account</span></span>
<span data-ttu-id="9cd3a-112">Określa nazwę konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="9cd3a-112">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cd3a-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9cd3a-113">-DatabaseName</span></span>
<span data-ttu-id="9cd3a-114">Określa nazwę bazy danych, która przechowuje poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="9cd3a-114">Specifies the name of the database that holds the credential.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cd3a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cd3a-115">-DefaultProfile</span></span>
<span data-ttu-id="9cd3a-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="9cd3a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9cd3a-117">-Force</span><span class="sxs-lookup"><span data-stu-id="9cd3a-117">-Force</span></span>
<span data-ttu-id="9cd3a-118">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="9cd3a-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9cd3a-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9cd3a-119">-Name</span></span>
<span data-ttu-id="9cd3a-120">Określa nazwę poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="9cd3a-120">Specifies the name of the credential.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cd3a-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9cd3a-121">-PassThru</span></span>
<span data-ttu-id="9cd3a-122">Wskazuje, że to polecenie cmdlet nie czeka na zakończenie operacji.</span><span class="sxs-lookup"><span data-stu-id="9cd3a-122">Indicates that this cmdlet does not wait for the operation to complete.</span></span>
<span data-ttu-id="9cd3a-123">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="9cd3a-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9cd3a-124">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="9cd3a-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9cd3a-125">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="9cd3a-125">-Password</span></span>
<span data-ttu-id="9cd3a-126">Hasło poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="9cd3a-126">The password for the credential.</span></span>
<span data-ttu-id="9cd3a-127">Jest to wymagane, Jeśli rozmówca nie jest właścicielem konta.</span><span class="sxs-lookup"><span data-stu-id="9cd3a-127">This is required if the caller is not the owner of the account.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cd3a-128">-Rekursywowanie</span><span class="sxs-lookup"><span data-stu-id="9cd3a-128">-Recurse</span></span>
<span data-ttu-id="9cd3a-129">Wskazuje, że operacja usuwania powinna przekroczyć, a także usunąć i upuścić wszystkie zasoby zależne od tego poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="9cd3a-129">Indicates that this delete operation should go through and also delete and drop all resources dependent on this credential.</span></span>

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

### <span data-ttu-id="9cd3a-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9cd3a-130">-Confirm</span></span>
<span data-ttu-id="9cd3a-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9cd3a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9cd3a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cd3a-132">-WhatIf</span></span>
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

### <span data-ttu-id="9cd3a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cd3a-133">CommonParameters</span></span>
<span data-ttu-id="9cd3a-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cd3a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cd3a-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cd3a-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cd3a-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9cd3a-136">INPUTS</span></span>

### <span data-ttu-id="9cd3a-137">System. String</span><span class="sxs-lookup"><span data-stu-id="9cd3a-137">System.String</span></span>

### <span data-ttu-id="9cd3a-138">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="9cd3a-138">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="9cd3a-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9cd3a-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9cd3a-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9cd3a-140">OUTPUTS</span></span>

### <span data-ttu-id="9cd3a-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9cd3a-141">System.Boolean</span></span>

## <span data-ttu-id="9cd3a-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9cd3a-142">NOTES</span></span>

## <span data-ttu-id="9cd3a-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9cd3a-143">RELATED LINKS</span></span>
